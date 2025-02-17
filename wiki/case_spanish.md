# [Linux] Bash case uso: Estructura de selección de patrones

## Overview
El comando `case` en Bash se utiliza para realizar selecciones de múltiples patrones. Permite ejecutar diferentes bloques de código dependiendo del valor de una variable, facilitando la toma de decisiones en scripts.

## Usage
La sintaxis básica del comando `case` es la siguiente:

```bash
case [variable] in
    [patrón1])
        # comandos para patrón1
        ;;
    [patrón2])
        # comandos para patrón2
        ;;
    *)
        # comandos por defecto
        ;;
esac
```

## Common Options
El comando `case` no tiene opciones específicas, pero se basa en patrones que puedes definir. Los patrones pueden incluir:

- `*`: Coincide con cualquier cadena.
- `?`: Coincide con un solo carácter.
- `[abc]`: Coincide con cualquier carácter dentro de los corchetes.

## Common Examples

### Ejemplo 1: Selección de días de la semana
```bash
dia="Lunes"

case $dia in
    "Lunes")
        echo "Hoy es lunes."
        ;;
    "Martes")
        echo "Hoy es martes."
        ;;
    "Miércoles")
        echo "Hoy es miércoles."
        ;;
    *)
        echo "No es un día de la semana válido."
        ;;
esac
```

### Ejemplo 2: Clasificación de números
```bash
numero=5

case $numero in
    1)
        echo "El número es uno."
        ;;
    2)
        echo "El número es dos."
        ;;
    3|4|5)
        echo "El número está entre tres y cinco."
        ;;
    *)
        echo "El número es mayor que cinco o menor que uno."
        ;;
esac
```

### Ejemplo 3: Comandos según extensión de archivo
```bash
archivo="documento.txt"

case $archivo in
    *.txt)
        echo "Es un archivo de texto."
        ;;
    *.jpg|*.png)
        echo "Es una imagen."
        ;;
    *)
        echo "Tipo de archivo desconocido."
        ;;
esac
```

## Tips
- Utiliza patrones específicos para mejorar la legibilidad de tu código.
- Recuerda cerrar cada bloque de comandos con `;;` para evitar errores de sintaxis.
- Puedes combinar patrones usando `|` para simplificar múltiples coincidencias.