# [Linux] Bash jobs Uso: Gerenciar processos em segundo plano

## Overview
O comando `jobs` no Bash é utilizado para listar os processos que estão sendo executados em segundo plano na sessão atual do terminal. Ele permite que os usuários vejam quais tarefas estão em execução, suas IDs de trabalho e seus estados.

## Usage
A sintaxe básica do comando `jobs` é a seguinte:

```bash
jobs [opções]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `jobs`:

- `-l`: Exibe os IDs de processo (PIDs) junto com os IDs de trabalho.
- `-n`: Mostra apenas os trabalhos que mudaram de estado desde a última execução do comando.
- `-p`: Exibe apenas os PIDs dos trabalhos.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `jobs`:

1. **Listar trabalhos em segundo plano**:
   ```bash
   jobs
   ```

2. **Listar trabalhos com IDs de processo**:
   ```bash
   jobs -l
   ```

3. **Listar apenas trabalhos que mudaram de estado**:
   ```bash
   jobs -n
   ```

4. **Obter apenas os PIDs dos trabalhos**:
   ```bash
   jobs -p
   ```

## Tips
- Utilize o comando `bg` para retomar um trabalho suspenso em segundo plano após usar `Ctrl+Z`.
- Combine o `jobs` com o comando `fg` para trazer um trabalho em segundo plano de volta para o primeiro plano.
- Lembre-se de que o comando `jobs` só lista os processos da sessão atual do terminal; processos de outras sessões não aparecerão.