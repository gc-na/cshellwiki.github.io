# [Linux] Bash if: Comprobar condiciones

## Overview
El comando `if` en Bash se utiliza para ejecutar comandos basados en la evaluación de condiciones. Permite tomar decisiones en los scripts, ejecutando diferentes bloques de código dependiendo de si una condición es verdadera o falsa.

## Usage
La sintaxis básica del comando `if` es la siguiente:

```bash
if [ condición ]; then
    # comandos a ejecutar si la condición es verdadera
else
    # comandos a ejecutar si la condición es falsa
fi
```

## Common Options
- `-e`: Verifica si un archivo existe.
- `-f`: Comprueba si un archivo es un archivo regular.
- `-d`: Verifica si un directorio existe.
- `-z`: Comprueba si una cadena está vacía.
- `-n`: Verifica si una cadena no está vacía.

## Common Examples

### Ejemplo 1: Comprobar si un archivo existe
```bash
if [ -e "archivo.txt" ]; then
    echo "El archivo existe."
else
    echo "El archivo no existe."
fi
```

### Ejemplo 2: Verificar si una variable está vacía
```bash
variable=""
if [ -z "$variable" ]; then
    echo "La variable está vacía."
else
    echo "La variable tiene contenido."
fi
```

### Ejemplo 3: Comprobar si un directorio existe
```bash
if [ -d "/ruta/al/directorio" ]; then
    echo "El directorio existe."
else
    echo "El directorio no existe."
fi
```

### Ejemplo 4: Comparar números
```bash
numero1=10
numero2=20
if [ $numero1 -lt $numero2 ]; then
    echo "$numero1 es menor que $numero2."
else
    echo "$numero1 no es menor que $numero2."
fi
```

## Tips
- Siempre utiliza espacios alrededor de los corchetes `[` y `]` para evitar errores de sintaxis.
- Puedes anidar múltiples condiciones utilizando `elif` para manejar más de dos casos.
- Recuerda cerrar la estructura `if` con `fi` para indicar el final de la condición.