# [Linux] Bash reboot uso: Reiniciar o sistema

## Overview
O comando `reboot` é utilizado para reiniciar o sistema operacional de forma segura. Ele encerra todos os processos em execução e reinicia a máquina, permitindo que as alterações de configuração ou atualizações sejam aplicadas.

## Usage
A sintaxe básica do comando `reboot` é a seguinte:

```bash
reboot [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `reboot`:

- `-f`: Força o reinício do sistema sem avisar os usuários ou encerrar os processos de forma adequada.
- `-p`: Desliga o sistema após o reinício. Esta opção é útil em sistemas que suportam desligamento.
- `--halt`: Para o sistema e o desliga, em vez de reiniciá-lo.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `reboot`:

1. **Reiniciar o sistema normalmente:**
   ```bash
   reboot
   ```

2. **Forçar o reinício sem avisos:**
   ```bash
   reboot -f
   ```

3. **Reiniciar e desligar o sistema após o reinício:**
   ```bash
   reboot -p
   ```

4. **Reiniciar o sistema com uma mensagem personalizada:**
   ```bash
   shutdown -r now "Reiniciando para aplicar atualizações"
   ```

## Tips
- Sempre salve seu trabalho antes de usar o comando `reboot`, especialmente se você estiver forçando o reinício.
- Utilize `shutdown` se você quiser ter mais controle sobre o processo de desligamento e reinício, permitindo que você avise os usuários.
- Verifique se você tem permissões adequadas para executar o comando `reboot`, pois ele geralmente requer privilégios de superusuário.