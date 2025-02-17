# [Linux] Bash break Uso: Interrompe loops

## Overview
O comando `break` é utilizado em scripts Bash para interromper a execução de loops. Quando o `break` é chamado dentro de um loop, ele encerra imediatamente o loop atual e continua a execução do código que vem após o loop.

## Usage
A sintaxe básica do comando `break` é a seguinte:

```bash
break [n]
```

Aqui, `n` é um número opcional que indica quantos níveis de loops devem ser interrompidos. Se `n` não for especificado, o `break` interrompe apenas o loop mais interno.

## Common Options
- `n`: Especifica o número de níveis de loops a serem interrompidos. Se não for fornecido, o padrão é 1.

## Common Examples

### Exemplo 1: Interrompendo um loop simples
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo $i
done
```
Neste exemplo, o loop imprime os números de 1 a 5, mas interrompe quando `i` é igual a 3. A saída será:
```
1
2
```

### Exemplo 2: Interrompendo um loop aninhado
```bash
for i in {1..3}; do
  for j in {1..3}; do
    if [ $j -eq 2 ]; then
      break 2
    fi
    echo "i: $i, j: $j"
  done
done
```
Aqui, o `break 2` interrompe ambos os loops. A saída será:
```
i: 1, j: 1
```

### Exemplo 3: Usando break em um while loop
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 4 ]; then
    break
  fi
  echo $count
  ((count++))
done
```
Neste exemplo, o loop `while` imprime os números de 1 a 5, mas para quando `count` é igual a 4. A saída será:
```
1
2
3
```

## Tips
- Use `break` com cuidado para evitar sair de loops inesperadamente, especialmente em loops aninhados.
- Sempre considere a lógica do seu script ao usar `break`, para garantir que a interrupção do loop não cause comportamentos indesejados.
- Para depuração, você pode adicionar mensagens de log antes do `break` para entender melhor o fluxo do seu script.