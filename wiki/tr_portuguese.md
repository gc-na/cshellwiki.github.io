# [Linux] Bash tr Uso equivalente: Transforma ou substitui caracteres

## Overview
O comando `tr` (translate) é utilizado para traduzir ou substituir caracteres em um fluxo de texto. Ele lê a entrada padrão, realiza as transformações especificadas e envia a saída para a saída padrão. É uma ferramenta útil para manipulação de texto em scripts e na linha de comando.

## Usage
A sintaxe básica do comando `tr` é a seguinte:

```bash
tr [opções] [argumentos]
```

## Common Options
- `-d`: Remove caracteres especificados.
- `-s`: Substitui sequências de caracteres repetidos por um único caractere.
- `-c`: Complementa o conjunto de caracteres especificados.
- `-t`: Especifica um conjunto de caracteres de tradução.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `tr`:

### Substituir caracteres
Substituindo todas as letras minúsculas por maiúsculas:

```bash
echo "olá mundo" | tr 'a-z' 'A-Z'
```

### Remover caracteres
Removendo todos os números de uma string:

```bash
echo "Texto 123 com números 456" | tr -d '0-9'
```

### Substituir múltiplos espaços por um único espaço
Substituindo sequências de espaços por um único espaço:

```bash
echo "Texto    com   múltiplos   espaços" | tr -s ' '
```

### Complementar caracteres
Substituindo todos os caracteres que não são letras:

```bash
echo "Texto!@# com caracteres especiais" | tr -c 'a-zA-Z' ' '
```

## Tips
- Utilize `tr` em combinação com outros comandos, como `grep` ou `awk`, para manipulações de texto mais complexas.
- Sempre teste seus comandos em um ambiente seguro antes de aplicá-los em arquivos importantes.
- Lembre-se de que `tr` não trabalha com arquivos diretamente; você deve usar redirecionamento ou pipes para fornecer a entrada.