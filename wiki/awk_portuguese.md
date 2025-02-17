# [Linux] Bash awk uso: Processamento e análise de texto

## Overview
O comando `awk` é uma poderosa ferramenta de processamento de texto e análise de dados em arquivos e streams. Ele permite que você manipule e extraia informações de linhas de texto de forma eficiente, utilizando uma linguagem de programação embutida.

## Usage
A sintaxe básica do comando `awk` é:

```bash
awk [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns do `awk`:

- `-F`: Define o delimitador de campo. Por exemplo, `-F,` para arquivos CSV.
- `-v`: Define variáveis antes da execução do script.
- `-f`: Especifica um arquivo que contém um script `awk`.
- `-W`: Ativa opções específicas do `awk`, como compatibilidade com versões anteriores.

## Common Examples

### Exemplo 1: Imprimir a primeira coluna de um arquivo
```bash
awk '{print $1}' arquivo.txt
```
Este comando imprime a primeira coluna de cada linha do arquivo `arquivo.txt`.

### Exemplo 2: Usar um delimitador de vírgula
```bash
awk -F, '{print $2}' dados.csv
```
Aqui, o comando imprime a segunda coluna de um arquivo CSV, onde as colunas são separadas por vírgulas.

### Exemplo 3: Filtrar linhas com uma condição
```bash
awk '$3 > 50 {print $1, $2}' arquivo.txt
```
Este exemplo imprime a primeira e a segunda coluna apenas das linhas onde o valor da terceira coluna é maior que 50.

### Exemplo 4: Contar o número de linhas
```bash
awk 'END {print NR}' arquivo.txt
```
Este comando conta e imprime o número total de linhas no arquivo `arquivo.txt`.

### Exemplo 5: Somar valores de uma coluna
```bash
awk '{soma += $2} END {print soma}' arquivo.txt
```
Aqui, o comando soma todos os valores da segunda coluna e imprime o total ao final.

## Tips
- Sempre verifique o delimitador correto ao trabalhar com arquivos de texto; use a opção `-F` para definir isso claramente.
- Teste seus scripts `awk` em pequenos arquivos antes de aplicá-los em grandes conjuntos de dados para evitar erros.
- Utilize variáveis para armazenar resultados intermediários e tornar seus scripts mais legíveis e organizados.