# [Linux] Bash gzip Uso: Compactar arquivos

## Overview
O comando `gzip` é utilizado para comprimir arquivos, reduzindo seu tamanho e economizando espaço em disco. Ele utiliza o algoritmo de compressão DEFLATE, que é eficiente e amplamente utilizado em sistemas Unix e Linux.

## Usage
A sintaxe básica do comando `gzip` é a seguinte:

```bash
gzip [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `gzip`:

- `-d` ou `--decompress`: Descomprime um arquivo.
- `-k` ou `--keep`: Mantém o arquivo original após a compressão.
- `-v` ou `--verbose`: Exibe informações detalhadas sobre o processo de compressão.
- `-r` ou `--recursive`: Comprime arquivos em diretórios de forma recursiva.

## Common Examples
Aqui estão alguns exemplos práticos de como usar o `gzip`:

1. **Comprimir um arquivo:**
   ```bash
   gzip arquivo.txt
   ```

2. **Descomprimir um arquivo:**
   ```bash
   gzip -d arquivo.txt.gz
   ```

3. **Manter o arquivo original ao comprimir:**
   ```bash
   gzip -k arquivo.txt
   ```

4. **Comprimir todos os arquivos em um diretório:**
   ```bash
   gzip -r /caminho/para/diretorio
   ```

5. **Exibir informações detalhadas durante a compressão:**
   ```bash
   gzip -v arquivo.txt
   ```

## Tips
- Sempre verifique o espaço em disco disponível antes de comprimir arquivos grandes.
- Utilize a opção `-k` se você precisar manter o arquivo original após a compressão.
- Para descomprimir arquivos `.gz`, você pode usar o comando `gunzip`, que é um atalho para `gzip -d`.