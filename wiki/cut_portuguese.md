# [Linux] Bash cut Uso: Extrair seções de linhas de texto

## Overview
O comando `cut` é utilizado para extrair seções específicas de linhas de texto em arquivos ou da entrada padrão. Ele é especialmente útil para manipular dados delimitados, como arquivos CSV ou TSV, permitindo que você selecione colunas ou caracteres específicos.

## Usage
A sintaxe básica do comando `cut` é a seguinte:

```bash
cut [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `cut`:

- `-f`: Especifica quais campos (colunas) extrair, usando um delimitador.
- `-d`: Define o delimitador que separa os campos. O padrão é a tabulação.
- `-c`: Extrai caracteres específicos, em vez de campos.
- `--complement`: Inverte a seleção, ou seja, extrai tudo, exceto os campos ou caracteres especificados.

## Common Examples

### Extrair campos de um arquivo CSV
Para extrair o segundo campo de um arquivo CSV onde os campos são separados por vírgulas:

```bash
cut -d ',' -f 2 arquivo.csv
```

### Extrair caracteres de uma linha
Para extrair os primeiros 5 caracteres de cada linha de um arquivo de texto:

```bash
cut -c 1-5 arquivo.txt
```

### Extrair múltiplos campos
Para extrair o primeiro e o terceiro campos de um arquivo TSV (separado por tabulações):

```bash
cut -f 1,3 arquivo.tsv
```

### Usar com entrada padrão
Você também pode usar `cut` com a entrada padrão. Por exemplo, para extrair o primeiro campo de uma lista de nomes separados por espaços:

```bash
echo -e "João Silva\nMaria Oliveira\nPedro Santos" | cut -d ' ' -f 1
```

## Tips
- Sempre verifique o delimitador do seu arquivo antes de usar `cut`, para garantir que você está extraindo os campos corretos.
- Combine `cut` com outros comandos, como `grep` ou `sort`, para manipulações mais complexas de dados.
- Use a opção `--complement` se você precisar excluir campos específicos em vez de selecioná-los.