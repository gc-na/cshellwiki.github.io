# [Linux] Bash cmp Uso: Compara arquivos byte a byte

## Overview
O comando `cmp` é utilizado para comparar dois arquivos byte a byte. Ele é útil para verificar se dois arquivos são idênticos ou para encontrar a primeira diferença entre eles.

## Usage
A sintaxe básica do comando `cmp` é a seguinte:

```
cmp [opções] [arquivo1] [arquivo2]
```

## Common Options
Aqui estão algumas opções comuns do `cmp`:

- `-l`: Lista as diferenças em formato octal.
- `-s`: Silencia a saída, apenas retorna o código de saída.
- `-i`: Ignora os primeiros N bytes de cada arquivo.
- `-n N`: Compara apenas os primeiros N bytes dos arquivos.

## Common Examples

1. Comparar dois arquivos e exibir a primeira diferença:
   ```bash
   cmp arquivo1.txt arquivo2.txt
   ```

2. Comparar dois arquivos sem exibir a saída, apenas o código de saída:
   ```bash
   cmp -s arquivo1.txt arquivo2.txt
   ```

3. Comparar os primeiros 10 bytes de dois arquivos:
   ```bash
   cmp -n 10 arquivo1.txt arquivo2.txt
   ```

4. Listar todas as diferenças em formato octal:
   ```bash
   cmp -l arquivo1.bin arquivo2.bin
   ```

5. Ignorar os primeiros 5 bytes de cada arquivo durante a comparação:
   ```bash
   cmp -i 5 arquivo1.txt arquivo2.txt
   ```

## Tips
- Use a opção `-s` quando você só precisa saber se os arquivos são diferentes, sem querer ver as diferenças.
- Para arquivos binários, a opção `-l` pode ser muito útil para entender as diferenças em um nível mais detalhado.
- Lembre-se de que `cmp` compara arquivos byte a byte, então mesmo uma pequena diferença resultará em uma saída indicando que os arquivos são diferentes.