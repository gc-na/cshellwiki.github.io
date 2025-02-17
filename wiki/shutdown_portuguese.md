# [Linux] Bash shutdown uso: Desligar o sistema

O comando `shutdown` é utilizado para desligar, reiniciar ou colocar o sistema em modo de espera.

## Overview
O comando `shutdown` permite que você desligue ou reinicie o sistema de forma segura. Ele notifica todos os usuários sobre a ação iminente e pode ser programado para ocorrer imediatamente ou em um horário específico.

## Usage
A sintaxe básica do comando é:

```bash
shutdown [opções] [tempo] [motivo]
```

## Common Options
- `-h` ou `--halt`: Desliga o sistema.
- `-r` ou `--reboot`: Reinicia o sistema.
- `-P` ou `--poweroff`: Desliga o sistema e desliga a energia.
- `now`: Executa a ação imediatamente.
- `+m`: Define um atraso em minutos antes de executar a ação.
- `hh:mm`: Define um horário específico para a ação.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `shutdown`:

1. Para desligar o sistema imediatamente:
   ```bash
   shutdown now
   ```

2. Para reiniciar o sistema imediatamente:
   ```bash
   shutdown -r now
   ```

3. Para desligar o sistema após 10 minutos:
   ```bash
   shutdown +10
   ```

4. Para agendar um desligamento para às 22:00:
   ```bash
   shutdown 22:00
   ```

5. Para desligar o sistema e enviar uma mensagem para todos os usuários:
   ```bash
   shutdown -h now "O sistema será desligado agora."
   ```

## Tips
- Sempre avise os usuários antes de desligar ou reiniciar o sistema para evitar perda de dados.
- Use o comando `shutdown -c` para cancelar um desligamento programado.
- Considere usar o comando `wall` para enviar uma mensagem a todos os usuários antes de um desligamento.