# [Linux] Bash expr Uso equivalente: Avaliação de expressões

## Overview
O comando `expr` é utilizado no Bash para avaliar expressões aritméticas, lógicas e de string. Ele permite realizar operações matemáticas simples, manipular strings e fazer comparações.

## Usage
A sintaxe básica do comando `expr` é a seguinte:

```bash
expr [opções] [argumentos]
```

## Common Options
- `-e`: Permite que você use expressões mais complexas.
- `length`: Retorna o comprimento de uma string.
- `index`: Retorna a posição da primeira ocorrência de uma substring em uma string.
- `match`: Verifica se uma string corresponde a uma expressão regular.

## Common Examples

### 1. Soma de dois números
```bash
expr 5 + 3
```
Saída: `8`

### 2. Subtração de dois números
```bash
expr 10 - 4
```
Saída: `6`

### 3. Multiplicação de dois números
```bash
expr 7 \* 6
```
Saída: `42`

### 4. Divisão de dois números
```bash
expr 20 / 4
```
Saída: `5`

### 5. Comprimento de uma string
```bash
expr length "Olá, Mundo!"
```
Saída: `12`

### 6. Encontrar a posição de uma substring
```bash
expr index "Bash Scripting" S
```
Saída: `6`

### 7. Comparação de dois números
```bash
expr 5 \> 3
```
Saída: `1` (verdadeiro)

## Tips
- Sempre escape o operador de multiplicação (`*`) com uma barra invertida (`\`) para evitar confusão com a expansão de globbing do shell.
- Use parênteses para agrupar expressões e controlar a ordem das operações.
- O `expr` retorna `0` para falso e `1` para verdadeiro em expressões de comparação.