# [Linux] Bash nohup Uso: Executar comandos que continuam rodando após o logout

## Overview
O comando `nohup` (no hang up) é utilizado para executar processos que devem continuar em execução mesmo após o usuário se desconectar do terminal. Isso é especialmente útil para longas tarefas que não precisam de interação contínua.

## Usage
A sintaxe básica do comando `nohup` é a seguinte:

```bash
nohup [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `nohup`:

- `&`: Coloca o comando em segundo plano, permitindo que você continue usando o terminal.
- `-h`: Exibe a ajuda sobre o uso do comando.
- `-v`: Ativa o modo verbose, mostrando mais informações sobre a execução.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `nohup`:

1. Executar um script em segundo plano:
   ```bash
   nohup ./meu_script.sh &
   ```

2. Rodar um comando que gera saída para um arquivo:
   ```bash
   nohup ping google.com > output.txt &
   ```

3. Executar um comando com um tempo limite:
   ```bash
   nohup sleep 1000 &
   ```

4. Iniciar um servidor web que deve continuar rodando:
   ```bash
   nohup python -m http.server 8000 &
   ```

## Tips
- Sempre redirecione a saída para um arquivo usando `>`, para evitar que a saída padrão seja enviada para o terminal.
- Use `jobs` para verificar os processos em segundo plano.
- Combine `nohup` com `disown` para desvincular o processo do terminal, permitindo que ele continue rodando após o logout.