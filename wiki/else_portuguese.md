# [Linux] Bash else uso equivalente: Estrutura condicional em scripts

## Overview
O comando `else` é utilizado em scripts Bash como parte de uma estrutura condicional. Ele permite que você especifique um bloco de código que será executado se a condição anterior (geralmente associada a um `if`) não for satisfeita. Isso é útil para controlar o fluxo de execução do seu script com base em condições específicas.

## Usage
A sintaxe básica do comando `else` é a seguinte:

```bash
if [ condição ]; then
    # comandos se a condição for verdadeira
else
    # comandos se a condição for falsa
fi
```

## Common Options
O comando `else` não possui opções específicas, pois é uma parte da estrutura condicional do Bash. No entanto, ele é frequentemente usado em conjunto com as seguintes construções:

- `if`: para verificar uma condição.
- `elif`: para testar condições adicionais antes de chegar ao `else`.

## Common Examples

### Exemplo 1: Verificando se um arquivo existe
```bash
if [ -f "meuarquivo.txt" ]; then
    echo "O arquivo existe."
else
    echo "O arquivo não existe."
fi
```

### Exemplo 2: Verificando a idade
```bash
idade=18
if [ $idade -ge 18 ]; then
    echo "Você é maior de idade."
else
    echo "Você é menor de idade."
fi
```

### Exemplo 3: Usando `elif` com `else`
```bash
nota=75
if [ $nota -ge 90 ]; then
    echo "Aprovado com distinção."
elif [ $nota -ge 60 ]; then
    echo "Aprovado."
else
    echo "Reprovado."
fi
```

## Tips
- Sempre use `fi` para fechar a estrutura condicional que começa com `if`.
- Mantenha a lógica clara e evite aninhar muitos `if` e `else` para facilitar a leitura do seu script.
- Utilize espaços ao redor dos colchetes `[` e `]` para garantir que o Bash interprete corretamente as condições.