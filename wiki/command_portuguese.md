# [Linux] Bash command uso: [executar comandos em segundo plano]

## Overview
O comando `nohup` permite que você execute um comando em segundo plano, mesmo após o fechamento da sessão do terminal. Isso é especialmente útil para longas execuções de scripts ou programas que você deseja que continuem rodando sem interrupção.

## Usage
A sintaxe básica do comando `nohup` é a seguinte:

```
nohup comando [opções] [argumentos] &
```

O símbolo `&` no final da linha indica que o comando deve ser executado em segundo plano.

## Common Options
- `&`: Coloca o comando em segundo plano.
- `-p`: Ignora o sinal SIGHUP (hangup) e permite que o processo continue rodando.
- `-c`: Permite que você especifique um comando a ser executado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `nohup`:

1. **Executar um script em segundo plano**:
   ```bash
   nohup ./meu_script.sh &
   ```

2. **Executar um comando longo e redirecionar a saída para um arquivo**:
   ```bash
   nohup long_running_command > output.log &
   ```

3. **Executar um comando com múltiplas opções**:
   ```bash
   nohup python meu_programa.py --opcao1 valor1 --opcao2 valor2 &
   ```

4. **Verificar a saída padrão e de erro**:
   ```bash
   nohup comando > saida.txt 2>&1 &
   ```

## Tips
- Sempre redirecione a saída para um arquivo para evitar que a saída padrão seja perdida.
- Use `jobs` para listar os processos em segundo plano e `fg` para trazê-los de volta ao primeiro plano, se necessário.
- Combine `nohup` com `disown` para garantir que o processo não seja encerrado ao sair do terminal.