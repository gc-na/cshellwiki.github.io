# [Linux] Bash no at: Agendar tarefas para execução futura

## Overview
O comando `at` é utilizado para agendar a execução de tarefas em um momento específico no futuro. Ele permite que os usuários programem comandos ou scripts para serem executados em horários determinados, facilitando a automação de tarefas.

## Usage
A sintaxe básica do comando `at` é a seguinte:

```bash
at [opções] [hora]
```

## Common Options
Aqui estão algumas opções comuns do comando `at`:

- `-f`: Especifica um arquivo de script a ser executado.
- `-m`: Envia um e-mail ao usuário após a execução do comando.
- `-q`: Define a fila de execução (padrão é 'a').
- `-l`: Lista os trabalhos agendados.
- `-d`: Remove um trabalho agendado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `at`:

1. **Agendar um comando para ser executado agora:**
   ```bash
   echo "echo 'Olá, mundo!'" | at now
   ```

2. **Agendar um comando para ser executado em uma hora:**
   ```bash
   echo "backup.sh" | at now + 1 hour
   ```

3. **Agendar um comando para ser executado em um horário específico:**
   ```bash
   echo "shutdown -h now" | at 22:00
   ```

4. **Agendar um script a partir de um arquivo:**
   ```bash
   at -f /caminho/para/script.sh now + 2 hours
   ```

5. **Listar trabalhos agendados:**
   ```bash
   at -l
   ```

6. **Remover um trabalho agendado:**
   ```bash
   at -d 1
   ```

## Tips
- Sempre verifique a lista de trabalhos agendados com `at -l` para evitar agendamentos duplicados.
- Utilize a opção `-m` para receber notificações por e-mail após a execução dos seus comandos.
- Para agendamentos recorrentes, considere usar o `cron`, que é mais adequado para tarefas repetitivas.