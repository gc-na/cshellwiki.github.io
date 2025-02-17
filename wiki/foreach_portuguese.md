# [Linux] Bash foreach uso equivalente: Executar comandos em uma lista

## Overview
O comando `foreach` é utilizado em alguns shells, como o C Shell, para iterar sobre uma lista de itens e executar um comando para cada um deles. Embora o Bash não tenha um comando `foreach` nativo, a mesma funcionalidade pode ser alcançada usando um loop `for`.

## Usage
A sintaxe básica para um loop `for` em Bash é a seguinte:

```bash
for item in [lista]; do
    [comando]
done
```

## Common Options
Embora o loop `for` em Bash não tenha opções específicas como o `foreach`, você pode usar algumas construções comuns, como:

- `in`: Especifica a lista de itens a serem iterados.
- `do`: Inicia o bloco de comandos que será executado para cada item.

## Common Examples

### Exemplo 1: Iterar sobre uma lista de números
```bash
for i in 1 2 3 4 5; do
    echo "Número: $i"
done
```

### Exemplo 2: Iterar sobre arquivos em um diretório
```bash
for arquivo in *.txt; do
    echo "Processando arquivo: $arquivo"
done
```

### Exemplo 3: Usar uma lista de strings
```bash
for fruta in maçã banana laranja; do
    echo "Fruta: $fruta"
done
```

### Exemplo 4: Executar um comando em cada diretório
```bash
for dir in /caminho/para/diretorios/*; do
    cd "$dir" && ls
done
```

## Tips
- Sempre use aspas ao redor de variáveis que podem conter espaços para evitar problemas de interpretação.
- Utilize `break` e `continue` dentro do loop para controlar o fluxo de execução.
- Teste seus comandos em um ambiente seguro antes de executá-los em produção, especialmente ao trabalhar com arquivos e diretórios.