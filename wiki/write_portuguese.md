# [Linux] Bash write uso equivalente: Enviar mensagens para outros usuários

## Overview
O comando `write` permite que um usuário envie mensagens de texto para outro usuário que esteja logado no mesmo sistema. É uma forma simples de comunicação em tempo real entre usuários em um ambiente de terminal.

## Usage
A sintaxe básica do comando `write` é a seguinte:

```bash
write [opções] [usuário] [terminal]
```

## Common Options
- `-n`: Não exibe o nome do usuário que está enviando a mensagem.
- `-s`: Envia a mensagem em modo silencioso, sem exibir o cabeçalho.

## Common Examples

1. **Enviar uma mensagem para um usuário específico:**
   Para enviar uma mensagem para o usuário `joao` que está logado no terminal `pts/1`, você pode usar:
   ```bash
   write joao pts/1
   ```
   Após executar este comando, você pode digitar sua mensagem e pressionar `Enter` para enviá-la.

2. **Enviar uma mensagem sem exibir o nome do usuário:**
   Para enviar uma mensagem sem mostrar seu nome, use a opção `-n`:
   ```bash
   write -n joao
   ```

3. **Usar o comando em modo silencioso:**
   Para enviar uma mensagem em modo silencioso, você pode usar a opção `-s`:
   ```bash
   write -s joao
   ```

## Tips
- Certifique-se de que o usuário destinatário esteja logado e que o terminal esteja ativo para receber a mensagem.
- Para encerrar a mensagem, pressione `Ctrl+D` ou `Ctrl+C`.
- Use o comando `who` para verificar quais usuários estão logados e onde eles estão, antes de enviar uma mensagem.