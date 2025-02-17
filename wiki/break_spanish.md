# [Linux] Bash break uso equivalente: Finaliza un bucle

## Overview
El comando `break` en Bash se utiliza para salir de un bucle anticipadamente. Esto es útil cuando se desea interrumpir la ejecución de un bucle antes de que se complete su ciclo normal, generalmente en función de una condición específica.

## Usage
La sintaxis básica del comando `break` es la siguiente:

```bash
break [n]
```

Donde `n` es un número opcional que indica cuántos niveles de bucles debe saltar. Si no se especifica, `break` saldrá del bucle más interno.

## Common Options
- `n`: Un número que especifica el nivel de bucle que se debe interrumpir. Si se omite, se interrumpe solo el bucle más interno.

## Common Examples

### Ejemplo 1: Salir de un bucle `for`
```bash
for i in {1..5}; do
  if [ $i -eq 3 ]; then
    break
  fi
  echo "Número: $i"
done
```
**Salida:**
```
Número: 1
Número: 2
```

### Ejemplo 2: Salir de un bucle `while`
```bash
count=1
while [ $count -le 5 ]; do
  if [ $count -eq 4 ]; then
    break
  fi
  echo "Contador: $count"
  ((count++))
done
```
**Salida:**
```
Contador: 1
Contador: 2
Contador: 3
```

### Ejemplo 3: Salir de bucles anidados
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
**Salida:**
```
i: 1, j: 1
```

## Tips
- Utiliza `break` cuando necesites salir de un bucle basado en una condición específica para evitar iteraciones innecesarias.
- Si trabajas con bucles anidados, especifica el número de niveles que deseas interrumpir para tener un control más preciso.
- Asegúrate de que el uso de `break` no interrumpa la lógica de tu script de manera inesperada.