# [Linux] Bash continue uso equivalente: Retomar a execução de um loop

## Overview
O comando `continue` no Bash é utilizado dentro de estruturas de repetição, como `for`, `while` e `until`, para pular a iteração atual e continuar com a próxima. Isso é útil quando você deseja ignorar certas condições sem sair completamente do loop.

## Usage
A sintaxe básica do comando `continue` é a seguinte:

```bash
continue [n]
```

Onde `n` é um número opcional que indica quantos níveis de loop devem ser ignorados. Se não for especificado, o padrão é 1.

## Common Options
- `n`: Um número que especifica quantos níveis de loop devem ser ignorados. Por exemplo, `continue 2` pulará a iteração atual do loop mais interno e continuará com o próximo nível externo.

## Common Examples

### Exemplo 1: Ignorando números ímpares
```bash
for i in {1..10}; do
  if (( i % 2 != 0 )); then
    continue
  fi
  echo $i
done
```
Neste exemplo, o loop imprime apenas os números pares de 1 a 10.

### Exemplo 2: Ignorando arquivos temporários
```bash
for file in *; do
  if [[ $file == *.tmp ]]; then
    continue
  fi
  echo "Processando $file"
done
```
Aqui, o loop processa todos os arquivos no diretório atual, exceto aqueles que têm a extensão `.tmp`.

### Exemplo 3: Usando `continue` em um loop `while`
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 3 ]; then
    count=$((count + 1))
    continue
  fi
  echo "Contagem: $count"
  count=$((count + 1))
done
```
Neste caso, o número 3 é ignorado na contagem, e o loop continua com os outros números.

## Tips
- Utilize `continue` para simplificar a lógica de loops, evitando a necessidade de aninhar condicionais.
- Sempre verifique se a condição que leva ao `continue` é clara, para que o código permaneça legível.
- Lembre-se de que o uso excessivo de `continue` pode tornar o fluxo do seu script mais difícil de seguir, então use-o com moderação.