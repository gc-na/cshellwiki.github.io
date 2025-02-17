# [Linux] Bash test uso: Avaliação de expressões

## Overview
O comando `test` é utilizado em Bash para avaliar expressões e condições. Ele permite verificar se um determinado arquivo existe, se uma string é vazia, se dois números são iguais, entre outras condições. O resultado da avaliação é retornado como um código de saída, onde um resultado verdadeiro retorna 0 e um falso retorna 1.

## Usage
A sintaxe básica do comando `test` é a seguinte:

```bash
test [opções] [argumentos]
```

## Common Options
Aqui estão algumas opções comuns que podem ser usadas com o comando `test`:

- `-e [arquivo]`: Verifica se o arquivo existe.
- `-f [arquivo]`: Verifica se o arquivo é um arquivo regular.
- `-d [diretório]`: Verifica se o argumento é um diretório.
- `-z [string]`: Verifica se a string é vazia.
- `-n [string]`: Verifica se a string não é vazia.
- `[string1] = [string2]`: Verifica se duas strings são iguais.
- `[número1] -eq [número2]`: Verifica se dois números são iguais.

## Common Examples
Aqui estão alguns exemplos práticos do uso do comando `test`:

### Verificar se um arquivo existe
```bash
test -e arquivo.txt && echo "O arquivo existe."
```

### Verificar se um diretório existe
```bash
test -d /caminho/para/diretorio && echo "O diretório existe."
```

### Verificar se uma string é vazia
```bash
string=""
test -z "$string" && echo "A string está vazia."
```

### Comparar duas strings
```bash
string1="teste"
string2="teste"
test "$string1" = "$string2" && echo "As strings são iguais."
```

### Comparar dois números
```bash
num1=5
num2=5
test $num1 -eq $num2 && echo "Os números são iguais."
```

## Tips
- Utilize `[` como uma alternativa ao comando `test`, pois ambos funcionam da mesma forma. Por exemplo, `[` é uma forma mais comum de escrever `test` em scripts.
- Sempre coloque aspas em torno de variáveis ao usar `test` para evitar erros com strings vazias.
- Combine múltiplas condições usando `-a` (E) e `-o` (OU) para avaliações mais complexas.