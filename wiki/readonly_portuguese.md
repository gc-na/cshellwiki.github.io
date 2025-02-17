# [Linux] Bash readonly uso: Define variáveis como somente leitura

## Overview
O comando `readonly` no Bash é utilizado para marcar variáveis como somente leitura. Uma vez que uma variável é definida como readonly, seu valor não pode ser alterado ou removido durante a execução do script ou da sessão do terminal.

## Usage
A sintaxe básica do comando `readonly` é a seguinte:

```bash
readonly [opções] [argumentos]
```

## Common Options
O comando `readonly` não possui muitas opções, mas aqui estão algumas que podem ser úteis:

- `-p`: Exibe uma lista de todas as variáveis que estão definidas como somente leitura.

## Common Examples

### Exemplo 1: Definindo uma variável como somente leitura
```bash
readonly VAR="valor"
```
Neste exemplo, a variável `VAR` é definida como somente leitura com o valor "valor".

### Exemplo 2: Tentando alterar uma variável somente leitura
```bash
readonly VAR="valor"
VAR="novo_valor"  # Isso resultará em um erro
```
Aqui, ao tentar alterar o valor de `VAR`, o Bash retornará um erro informando que a variável é somente leitura.

### Exemplo 3: Listando variáveis somente leitura
```bash
readonly -p
```
Este comando exibirá todas as variáveis que foram definidas como somente leitura na sessão atual.

## Tips
- Utilize `readonly` para proteger variáveis que não devem ser alteradas acidentalmente, especialmente em scripts complexos.
- Lembre-se de que uma variável marcada como somente leitura não pode ser removida ou alterada, então use essa funcionalidade com cautela.
- Para remover a proteção de uma variável, você precisará reiniciar a sessão ou criar uma nova variável com um nome diferente.