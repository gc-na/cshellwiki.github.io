# [Linux] Bash mountpoint uso: Verifica se um diretório é um ponto de montagem

## Overview
O comando `mountpoint` é utilizado para verificar se um diretório específico é um ponto de montagem de um sistema de arquivos. Isso é útil para administradores de sistema que precisam confirmar a configuração de montagens em um sistema Linux.

## Usage
A sintaxe básica do comando é a seguinte:

```bash
mountpoint [opções] [argumentos]
```

## Common Options
- `-q`: Executa a verificação em modo silencioso, sem saída de mensagem.
- `-d`: Exibe informações detalhadas sobre o ponto de montagem.
- `--help`: Mostra a ajuda do comando e as opções disponíveis.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `mountpoint`:

1. Verificar se um diretório é um ponto de montagem:
   ```bash
   mountpoint /mnt
   ```

2. Usar o modo silencioso para verificar um ponto de montagem:
   ```bash
   mountpoint -q /mnt
   ```

3. Obter informações detalhadas sobre um ponto de montagem:
   ```bash
   mountpoint -d /mnt
   ```

4. Verificar múltiplos diretórios ao mesmo tempo:
   ```bash
   mountpoint /mnt /media
   ```

## Tips
- Utilize a opção `-q` se você deseja apenas um retorno de sucesso ou falha sem mensagens adicionais, ideal para scripts.
- Sempre verifique se o diretório que você está testando realmente existe para evitar mensagens de erro desnecessárias.
- Combine o `mountpoint` com outros comandos, como `if`, para criar scripts que automatizem a verificação de montagens.