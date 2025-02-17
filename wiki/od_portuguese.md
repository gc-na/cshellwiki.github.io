# [Linux] Bash od: Exibir conteúdo de arquivos em diferentes formatos

## Overview
O comando `od` (octal dump) é utilizado para exibir o conteúdo de arquivos em diferentes formatos, como octal, hexadecimal, decimal e ASCII. Ele é especialmente útil para analisar arquivos binários ou para depuração.

## Usage
A sintaxe básica do comando `od` é a seguinte:

```
od [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `od`:

- `-A, --address-radix=RADIX`: Define a base para os endereços. As opções incluem `d` (decimal), `o` (octal), `x` (hexadecimal).
- `-t, --format=FORMATO`: Especifica o formato de saída. Exemplos incluem `c` (caractere), `d` (decimal), `o` (octal), `x` (hexadecimal).
- `-N, --read-bytes=N`: Lê apenas os primeiros N bytes do arquivo.
- `-v, --output-duplicates`: Exibe todos os dados, incluindo duplicatas.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `od`:

1. **Exibir conteúdo em formato octal:**
   ```bash
   od arquivo.bin
   ```

2. **Exibir conteúdo em formato hexadecimal:**
   ```bash
   od -t x1 arquivo.bin
   ```

3. **Exibir os primeiros 16 bytes de um arquivo:**
   ```bash
   od -N 16 arquivo.bin
   ```

4. **Exibir conteúdo em formato decimal:**
   ```bash
   od -t d1 arquivo.bin
   ```

5. **Exibir conteúdo com endereços em hexadecimal:**
   ```bash
   od -A x arquivo.bin
   ```

## Tips
- Utilize a opção `-v` para garantir que todos os dados sejam mostrados, mesmo que haja duplicatas.
- Combine opções para personalizar a saída de acordo com suas necessidades, como `od -A x -t x1 arquivo.bin`.
- Para arquivos de texto, o `od` pode ser útil para visualizar caracteres não imprimíveis.