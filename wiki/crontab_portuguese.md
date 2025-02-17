# [Linux] Bash crontab Uso: Agendar tarefas automaticamente

## Overview
O comando `crontab` é utilizado para agendar tarefas que devem ser executadas automaticamente em intervalos regulares no sistema operacional Linux. Ele permite que os usuários configurem comandos ou scripts para serem executados em horários específicos, facilitando a automação de tarefas repetitivas.

## Usage
A sintaxe básica do comando `crontab` é a seguinte:

```bash
crontab [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `crontab`:

- `-e`: Edita o arquivo crontab do usuário atual.
- `-l`: Lista as entradas do crontab do usuário atual.
- `-r`: Remove o arquivo crontab do usuário atual.
- `-i`: Solicita confirmação antes de remover o crontab.

## Common Examples
Aqui estão alguns exemplos práticos do uso do `crontab`:

1. **Editar o crontab**:
   Para editar o crontab do usuário atual, use:
   ```bash
   crontab -e
   ```

2. **Listar tarefas agendadas**:
   Para listar todas as tarefas agendadas, use:
   ```bash
   crontab -l
   ```

3. **Remover o crontab**:
   Para remover todas as tarefas agendadas, use:
   ```bash
   crontab -r
   ```

4. **Agendar uma tarefa para ser executada todos os dias às 2h**:
   Para executar um script chamado `backup.sh` todos os dias às 2h da manhã, adicione a seguinte linha ao crontab:
   ```bash
   0 2 * * * /caminho/para/backup.sh
   ```

5. **Agendar uma tarefa a cada 15 minutos**:
   Para executar um comando a cada 15 minutos, adicione:
   ```bash
   */15 * * * * comando
   ```

## Tips
- Sempre verifique se o caminho para os scripts ou comandos está correto.
- Use redirecionamento de saída para registrar logs de tarefas agendadas, como:
  ```bash
  0 2 * * * /caminho/para/backup.sh >> /caminho/para/logs/backup.log 2>&1
  ```
- Teste seus comandos manualmente antes de agendá-los para evitar erros.