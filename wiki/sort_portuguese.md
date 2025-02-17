# [Linux] Bash sort uso: Ordenar linhas de texto

## Overview
O comando `sort` no Bash é utilizado para ordenar linhas de texto em arquivos ou na saída de outros comandos. Ele organiza as linhas em ordem alfabética ou numérica, facilitando a leitura e análise de dados.

## Usage
A sintaxe básica do comando `sort` é a seguinte:

```bash
sort [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do comando `sort`:

- `-r`: Ordena as linhas em ordem reversa.
- `-n`: Ordena as linhas numericamente.
- `-k`: Especifica a coluna a ser usada para a ordenação.
- `-u`: Remove linhas duplicadas após a ordenação.
- `-o`: Escreve a saída em um arquivo especificado.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `sort`:

1. **Ordenar um arquivo em ordem alfabética:**
   ```bash
   sort arquivo.txt
   ```

2. **Ordenar um arquivo em ordem reversa:**
   ```bash
   sort -r arquivo.txt
   ```

3. **Ordenar um arquivo numericamente:**
   ```bash
   sort -n numeros.txt
   ```

4. **Ordenar e remover duplicatas:**
   ```bash
   sort -u arquivo.txt
   ```

5. **Ordenar com base em uma coluna específica:**
   ```bash
   sort -k 2 arquivo.txt
   ```

6. **Salvar a saída ordenada em um novo arquivo:**
   ```bash
   sort arquivo.txt -o arquivo_ordenado.txt
   ```

## Tips
- Sempre verifique se o arquivo de entrada não contém caracteres especiais que possam interferir na ordenação.
- Utilize a opção `-k` para ordenar por colunas específicas em arquivos delimitados, como CSV.
- Combine o `sort` com outros comandos, como `uniq`, para uma análise de dados mais eficiente.