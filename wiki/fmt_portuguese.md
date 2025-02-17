# [Linux] Bash fmt Uso: Formatação de texto

## Overview
O comando `fmt` é utilizado para formatar texto em arquivos ou na entrada padrão, ajustando a largura das linhas e facilitando a leitura. Ele é especialmente útil para preparar textos que serão exibidos em ambientes com largura de coluna limitada.

## Usage
A sintaxe básica do comando `fmt` é a seguinte:

```bash
fmt [opções] [arquivos]
```

Se nenhum arquivo for especificado, o `fmt` lê da entrada padrão.

## Common Options
Aqui estão algumas opções comuns do comando `fmt`:

- `-w N`: Define a largura máxima das linhas para N caracteres.
- `-s`: Não quebra linhas que já estão dentro da largura especificada.
- `-p`: Indenta cada parágrafo com um espaço em branco.
- `-u`: Remove espaços em branco adicionais entre palavras.

## Common Examples

### Exemplo 1: Formatar um arquivo de texto
Para formatar um arquivo chamado `texto.txt` com uma largura de linha de 50 caracteres, você pode usar:

```bash
fmt -w 50 texto.txt
```

### Exemplo 2: Formatar texto da entrada padrão
Você pode usar o `fmt` para formatar texto diretamente da entrada padrão:

```bash
echo "Este é um exemplo de texto que será formatado pelo comando fmt." | fmt -w 40
```

### Exemplo 3: Indentação de parágrafos
Para indentar parágrafos em um arquivo chamado `documento.txt`, você pode usar:

```bash
fmt -p documento.txt
```

### Exemplo 4: Remover espaços em branco
Para formatar um texto e remover espaços em branco adicionais, você pode usar:

```bash
fmt -u texto.txt
```

## Tips
- Sempre verifique a largura das linhas com a opção `-w` para garantir que o texto se ajuste ao seu ambiente.
- Use a opção `-s` se você quiser manter a formatação original de linhas longas.
- Combine o `fmt` com outros comandos, como `cat`, para manipular e formatar texto de maneira mais eficiente.