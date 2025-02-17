# [Linux] Bash nice uso: Ajusta a prioridade de execução de processos

## Overview
O comando `nice` é utilizado no sistema operacional Linux para alterar a prioridade de execução de processos. Ele permite que o usuário inicie um comando com uma prioridade diferente, o que pode ser útil para gerenciar a carga do sistema e garantir que processos importantes recebam mais recursos.

## Usage
A sintaxe básica do comando `nice` é a seguinte:

```
nice [opções] [comando]
```

## Common Options
Aqui estão algumas opções comuns do `nice`:

- `-n, --adjustment=N`: Define o valor de ajuste da prioridade. O valor padrão é 10. Valores negativos aumentam a prioridade, enquanto valores positivos a diminuem.
- `-h, --help`: Exibe uma mensagem de ajuda com informações sobre o comando.
- `--version`: Mostra a versão do comando `nice`.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `nice`:

1. Iniciar um processo com prioridade padrão:
   ```bash
   nice comando
   ```

2. Iniciar um processo com prioridade reduzida (aumentando o valor de nice):
   ```bash
   nice -n 10 comando
   ```

3. Iniciar um processo com prioridade aumentada (diminuindo o valor de nice):
   ```bash
   nice -n -5 comando
   ```

4. Verificar a prioridade de um processo em execução:
   ```bash
   ps -o pid,ni,cmd
   ```

## Tips
- Use `nice` para processos que não são críticos, permitindo que outros processos mais importantes tenham prioridade.
- Combine `nice` com o comando `renice` para alterar a prioridade de processos já em execução.
- Lembre-se de que apenas usuários com permissões adequadas podem aumentar a prioridade de um processo (valores negativos).