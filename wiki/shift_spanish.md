# [Linux] Bash shift Uso equivalente: Mover parámetros a la izquierda

El comando `shift` se utiliza en Bash para desplazar los parámetros posicionales a la izquierda, lo que permite acceder a los argumentos de un script o función de manera más sencilla.

## Overview
El comando `shift` elimina el primer parámetro posicional (el que está en la posición 1) y desplaza todos los demás parámetros hacia la izquierda. Esto significa que después de ejecutar `shift`, el segundo parámetro se convierte en el primero, el tercero en el segundo, y así sucesivamente.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
shift [n]
```

Donde `n` es el número de posiciones que se desea desplazar. Si `n` no se especifica, el valor predeterminado es 1.

## Common Options
- `n`: Especifica cuántas posiciones se deben desplazar. Si se omite, se desplaza 1 por defecto.

## Common Examples

### Ejemplo 1: Desplazar un parámetro
```bash
#!/bin/bash
echo "Antes de shift: \$1 = $1"
shift
echo "Después de shift: \$1 = $1"
```
Si ejecutas el script con `./script.sh uno dos tres`, la salida será:
```
Antes de shift: $1 = uno
Después de shift: $1 = dos
```

### Ejemplo 2: Desplazar múltiples parámetros
```bash
#!/bin/bash
echo "Antes de shift: \$1 = $1, \$2 = $2"
shift 2
echo "Después de shift: \$1 = $1, \$2 = $2"
```
Si ejecutas el script con `./script.sh uno dos tres cuatro`, la salida será:
```
Antes de shift: $1 = uno, $2 = dos
Después de shift: $1 = tres, $2 = cuatro
```

### Ejemplo 3: Uso en un bucle
```bash
#!/bin/bash
while [[ $# -gt 0 ]]; do
  echo "Parámetro: $1"
  shift
done
```
Si ejecutas el script con `./script.sh uno dos tres`, la salida será:
```
Parámetro: uno
Parámetro: dos
Parámetro: tres
```

## Tips
- Utiliza `shift` en scripts que manejan múltiples parámetros para simplificar el acceso a ellos.
- Considera usar `shift` dentro de bucles para procesar todos los argumentos de forma secuencial.
- Recuerda que después de usar `shift`, el número total de parámetros (`$#`) se reduce, así que verifica su valor si necesitas saber cuántos quedan.