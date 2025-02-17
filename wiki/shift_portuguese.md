# [Linux] Bash shift Uso equivalente: Manipula parâmetros de posição

## Overview
O comando `shift` é utilizado em scripts Bash para manipular parâmetros de posição. Ele desloca os parâmetros para a esquerda, permitindo que você acesse os argumentos passados para o script de forma mais conveniente.

## Usage
A sintaxe básica do comando `shift` é a seguinte:

```bash
shift [n]
```

Onde `n` é o número de posições a serem deslocadas. Se `n` não for especificado, o padrão é 1.

## Common Options
- `n`: Especifica quantas posições os parâmetros devem ser deslocados. Se não for fornecido, o padrão é 1.

## Common Examples

### Exemplo 1: Uso básico do shift
```bash
#!/bin/bash
echo "Parâmetro 1: $1"
echo "Parâmetro 2: $2"
shift
echo "Após shift:"
echo "Parâmetro 1: $1"
echo "Parâmetro 2: $2"
```
Neste exemplo, o primeiro parâmetro é deslocado, e o segundo parâmetro se torna o primeiro.

### Exemplo 2: Deslocando múltiplos parâmetros
```bash
#!/bin/bash
echo "Parâmetro 1: $1"
echo "Parâmetro 2: $2"
shift 2
echo "Após shift 2:"
echo "Parâmetro 1: $1"
echo "Parâmetro 2: $2"
```
Aqui, dois parâmetros são deslocados, permitindo que o terceiro parâmetro se torne o primeiro.

### Exemplo 3: Loop com shift
```bash
#!/bin/bash
while [[ $# -gt 0 ]]; do
    echo "Processando: $1"
    shift
done
```
Este exemplo demonstra como usar `shift` em um loop para processar todos os parâmetros passados para o script.

## Tips
- Use `shift` quando precisar processar argumentos de forma sequencial em scripts.
- Sempre verifique o número de parâmetros restantes (`$#`) antes de usar `shift` para evitar erros.
- Combine `shift` com outros comandos, como `case` ou `while`, para criar scripts mais dinâmicos e interativos.