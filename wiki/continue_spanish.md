# [Linux] Bash continue uso: Continuar con el siguiente ciclo en un bucle

## Overview
El comando `continue` en Bash se utiliza dentro de estructuras de control de bucle, como `for`, `while` y `until`. Su función principal es omitir el resto del código en la iteración actual del bucle y continuar con la siguiente iteración.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
continue [n]
```

Donde `n` es un número opcional que especifica cuántas iteraciones del bucle se deben omitir. Si no se proporciona un número, se omite solo la iteración actual.

## Common Options
- `n`: Especifica cuántas iteraciones del bucle se deben omitir. Por defecto, se omite solo la iteración actual.

## Common Examples

### Ejemplo 1: Usar continue en un bucle for
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        continue
    fi
    echo "Número: $i"
done
```
**Salida:**
```
Número: 1
Número: 2
Número: 4
Número: 5
```
En este ejemplo, cuando `i` es igual a 3, se omite esa iteración y se continúa con el siguiente número.

### Ejemplo 2: Usar continue en un bucle while
```bash
contador=1
while [ $contador -le 5 ]; do
    if [ $contador -eq 2 ]; then
        contador=$((contador + 1))
        continue
    fi
    echo "Contador: $contador"
    contador=$((contador + 1))
done
```
**Salida:**
```
Contador: 1
Contador: 3
Contador: 4
Contador: 5
```
Aquí, cuando el contador es 2, se omite esa iteración y se continúa con el siguiente número.

### Ejemplo 3: Usar continue con un número
```bash
for i in {1..10}; do
    if [ $i -lt 5 ]; then
        continue 2
    fi
    echo "Número: $i"
done
```
**Salida:**
```
Número: 5
Número: 6
Número: 7
Número: 8
Número: 9
Número: 10
```
En este caso, al usar `continue 2`, se omiten las dos primeras iteraciones del bucle.

## Tips
- Utiliza `continue` para mejorar la legibilidad de tu código al evitar bloques anidados innecesarios.
- Asegúrate de que el uso de `continue` no cause bucles infinitos. Verifica las condiciones de salida adecuadamente.
- Es una buena práctica documentar el uso de `continue` en tus scripts para que otros desarrolladores comprendan la lógica detrás de su uso.