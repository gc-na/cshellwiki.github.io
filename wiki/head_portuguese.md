# [Linux] Bash head uso: Exibir as primeiras linhas de arquivos

## Overview
O comando `head` é utilizado para exibir as primeiras linhas de um ou mais arquivos. Por padrão, ele mostra as primeiras 10 linhas, mas é possível modificar essa quantidade conforme necessário.

## Usage
A sintaxe básica do comando `head` é a seguinte:

```bash
head [opções] [arquivos]
```

## Common Options
Aqui estão algumas opções comuns do comando `head`:

- `-n [número]`: Especifica o número de linhas a serem exibidas. Por exemplo, `-n 5` mostrará as primeiras 5 linhas.
- `-c [número]`: Exibe os primeiros bytes do arquivo. Por exemplo, `-c 20` mostrará os primeiros 20 bytes.
- `-q`: Suprime a impressão do cabeçalho dos arquivos quando múltiplos arquivos são fornecidos.
- `-v`: Sempre imprime o cabeçalho dos arquivos, mesmo que apenas um arquivo seja fornecido.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `head`:

1. Exibir as primeiras 10 linhas de um arquivo chamado `exemplo.txt`:

    ```bash
    head exemplo.txt
    ```

2. Exibir as primeiras 5 linhas de um arquivo:

    ```bash
    head -n 5 exemplo.txt
    ```

3. Exibir os primeiros 15 bytes de um arquivo:

    ```bash
    head -c 15 exemplo.txt
    ```

4. Exibir as primeiras 10 linhas de múltiplos arquivos:

    ```bash
    head arquivo1.txt arquivo2.txt
    ```

5. Exibir as primeiras linhas de um arquivo e sempre mostrar o cabeçalho:

    ```bash
    head -v exemplo.txt
    ```

## Tips
- Use `head` em combinação com outros comandos, como `grep`, para filtrar e visualizar rapidamente as primeiras linhas de resultados específicos.
- Lembre-se de que o `head` pode ser útil para verificar rapidamente o conteúdo de arquivos grandes sem precisar abri-los completamente.
- Para uma visualização mais completa, considere usar `tail` em conjunto com `head` para comparar as primeiras e últimas linhas de um arquivo.