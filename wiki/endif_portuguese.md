# [Linux] Bash endif equivalente: Finaliza um bloco condicional

## Overview
O comando `endif` é utilizado em scripts de shell para finalizar um bloco condicional iniciado com `if`. Ele é parte da estrutura de controle de fluxo que permite a execução condicional de comandos.

## Usage
A sintaxe básica do comando `endif` é a seguinte:

```bash
endif
```

## Common Options
O comando `endif` não possui opções específicas, pois sua função é simplesmente finalizar um bloco `if`. No entanto, é importante lembrar que ele deve ser usado corretamente dentro de uma estrutura condicional.

## Common Examples

### Exemplo 1: Estrutura básica de if
```bash
if [ "$VAR" -eq 1 ]; then
    echo "A variável é igual a 1"
endif
```

### Exemplo 2: Usando if com else
```bash
if [ "$VAR" -eq 1 ]; then
    echo "A variável é igual a 1"
else
    echo "A variável não é igual a 1"
endif
```

### Exemplo 3: Estrutura if aninhada
```bash
if [ "$VAR" -eq 1 ]; then
    echo "A variável é igual a 1"
    if [ "$VAR2" -eq 2 ]; then
        echo "A variável 2 é igual a 2"
    endif
endif
```

## Tips
- Sempre use `endif` para garantir que o bloco condicional seja fechado corretamente.
- Mantenha a indentação consistente para facilitar a leitura do seu código.
- Teste suas condições antes de usar `endif` para evitar erros de lógica no seu script.