# [Linux] Bash else uso equivalente: Estructura condicional en scripts

## Overview
El comando `else` en Bash se utiliza como parte de una estructura condicional. Permite ejecutar un bloque de código alternativo si la condición previa no se cumple. Es una herramienta fundamental para el control de flujo en scripts de Bash.

## Usage
La sintaxis básica del comando `else` es la siguiente:

```bash
if [ condición ]; then
    # Código si la condición es verdadera
else
    # Código si la condición es falsa
fi
```

## Common Options
El comando `else` en sí mismo no tiene opciones, ya que es parte de la estructura de control `if`. Sin embargo, puedes combinarlo con diversas condiciones y comandos dentro del bloque `if`.

## Common Examples

### Ejemplo 1: Comprobación de un archivo
```bash
if [ -f "archivo.txt" ]; then
    echo "El archivo existe."
else
    echo "El archivo no existe."
fi
```

### Ejemplo 2: Comprobación de una variable
```bash
nombre="Juan"
if [ "$nombre" == "Pedro" ]; then
    echo "Hola, Pedro."
else
    echo "Hola, $nombre."
fi
```

### Ejemplo 3: Comprobación de un número
```bash
numero=10
if [ "$numero" -gt 5 ]; then
    echo "El número es mayor que 5."
else
    echo "El número es 5 o menor."
fi
```

## Tips
- Asegúrate de cerrar siempre la estructura `if` con `fi` para evitar errores de sintaxis.
- Puedes anidar múltiples condiciones usando `elif` junto con `else` para manejar más de dos casos.
- Utiliza espacios alrededor de los corchetes en las condiciones para mejorar la legibilidad.