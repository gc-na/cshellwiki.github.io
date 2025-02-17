# [Linux] Bash renice Uso: Ajustar a prioridade de processos em execução

## Overview
O comando `renice` é utilizado para alterar a prioridade de execução de processos já em execução no sistema. A prioridade determina a quantidade de tempo de CPU que um processo recebe em relação a outros processos. Um valor de prioridade mais baixo significa maior prioridade.

## Usage
A sintaxe básica do comando `renice` é a seguinte:

```bash
renice [opções] [valores de prioridade] [PID]
```

## Common Options
- `-n`: Define o novo valor de prioridade. O valor pode ser um número negativo (para aumentar a prioridade) ou positivo (para diminuir a prioridade).
- `-p`: Especifica o PID (Identificador do Processo) do processo cuja prioridade você deseja alterar.
- `-g`: Permite alterar a prioridade de todos os processos pertencentes a um grupo de processos.
- `-u`: Altera a prioridade de todos os processos pertencentes a um usuário específico.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o comando `renice`:

1. **Alterar a prioridade de um processo específico:**
   Para aumentar a prioridade (reduzir o valor de prioridade) de um processo com PID 1234:
   ```bash
   renice -n -5 -p 1234
   ```

2. **Reduzir a prioridade de um processo:**
   Para diminuir a prioridade (aumentar o valor de prioridade) de um processo com PID 5678:
   ```bash
   renice -n 10 -p 5678
   ```

3. **Alterar a prioridade de todos os processos de um usuário:**
   Para alterar a prioridade de todos os processos do usuário "joao" para 5:
   ```bash
   renice -n 5 -u joao
   ```

4. **Alterar a prioridade de todos os processos em um grupo:**
   Para alterar a prioridade de todos os processos no grupo de processos com GID 1000:
   ```bash
   renice -n 0 -g 1000
   ```

## Tips
- Sempre verifique a prioridade atual dos processos antes de usar o `renice`, utilizando o comando `ps` ou `top`.
- Use valores de prioridade com cuidado, pois aumentar a prioridade de um processo pode afetar o desempenho de outros processos no sistema.
- Para aplicar mudanças de prioridade, você pode precisar de permissões de superusuário, especialmente ao alterar a prioridade de processos que não pertencem ao seu usuário.