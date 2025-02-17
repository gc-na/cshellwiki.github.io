# [Linux] Bash comm uso: compara arquivos linha a linha

## Overview
O comando `comm` é utilizado para comparar duas ou mais listas de texto, exibindo as linhas que são exclusivas de cada arquivo, bem como as linhas que são comuns entre eles. Ele é especialmente útil para identificar diferenças e semelhanças em arquivos de texto.

## Usage
A sintaxe básica do comando `comm` é a seguinte:

```bash
comm [opções] [arquivo1] [arquivo2]
```

## Common Options
- `-1`: Suprime a saída das linhas que estão apenas no primeiro arquivo.
- `-2`: Suprime a saída das linhas que estão apenas no segundo arquivo.
- `-3`: Suprime a saída das linhas que estão em ambos os arquivos.
- `-i`: Ignora a diferença entre maiúsculas e minúsculas ao comparar as linhas.
- `-d`: Exibe as linhas duplicadas.

## Common Examples

1. **Comparar dois arquivos e mostrar todas as linhas:**
   ```bash
   comm arquivo1.txt arquivo2.txt
   ```

2. **Mostrar apenas as linhas que estão no primeiro arquivo:**
   ```bash
   comm -13 arquivo1.txt arquivo2.txt
   ```

3. **Mostrar apenas as linhas que estão no segundo arquivo:**
   ```bash
   comm -12 arquivo1.txt arquivo2.txt
   ```

4. **Comparar arquivos ignorando maiúsculas e minúsculas:**
   ```bash
   comm -i arquivo1.txt arquivo2.txt
   ```

5. **Comparar e mostrar apenas as linhas duplicadas:**
   ```bash
   comm -d arquivo1.txt arquivo2.txt
   ```

## Tips
- Certifique-se de que os arquivos estejam ordenados antes de usar o comando `comm`, pois ele compara as linhas na ordem em que aparecem.
- Utilize o comando `sort` para ordenar os arquivos antes da comparação, caso necessário:
  ```bash
  sort arquivo1.txt -o arquivo1.txt
  sort arquivo2.txt -o arquivo2.txt
  comm arquivo1.txt arquivo2.txt
  ```
- Experimente combinar `comm` com outros comandos, como `grep`, para filtrar ainda mais os resultados da comparação.