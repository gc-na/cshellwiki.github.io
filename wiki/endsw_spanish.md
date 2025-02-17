# [Linux] Bash endsw uso: Finaliza un script o un bloque de código

## Overview
El comando `endsw` en Bash se utiliza para finalizar un script o un bloque de código que se ha iniciado con una instrucción de control como `case`. Es útil para estructurar el flujo de un script y asegurar que se ejecute correctamente.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
endsw
```

## Common Options
El comando `endsw` no tiene opciones específicas, ya que su función principal es simplemente marcar el final de un bloque de código. Sin embargo, se utiliza en conjunto con otras instrucciones de control.

## Common Examples

### Ejemplo 1: Uso básico en un script
```bash
#!/bin/bash

case $1 in
    "opcion1")
        echo "Has elegido la opción 1"
        ;;
    "opcion2")
        echo "Has elegido la opción 2"
        ;;
    *)
        echo "Opción no válida"
        ;;
esac
```
En este ejemplo, `endsw` se utiliza implícitamente al finalizar el bloque `case` con `esac`.

### Ejemplo 2: Combinación con otras estructuras
```bash
#!/bin/bash

read -p "Introduce un número: " numero

case $numero in
    1)
        echo "Uno"
        ;;
    2)
        echo "Dos"
        ;;
    3)
        echo "Tres"
        ;;
    *)
        echo "Número no reconocido"
        ;;
esac
```
Aquí, el bloque `case` se cierra con `esac`, que es el equivalente a `endsw`.

## Tips
- Asegúrate de que cada bloque de control que inicies tenga su correspondiente finalización para evitar errores de sintaxis.
- Utiliza comentarios para aclarar la lógica de tus bloques de código, especialmente en scripts más largos.
- Prueba tus scripts en un entorno seguro antes de ejecutarlos en producción para asegurarte de que funcionan como se espera.