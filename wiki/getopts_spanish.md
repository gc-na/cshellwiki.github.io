# [Linux] Bash getopts Uso: [analizar opciones de línea de comandos]

## Overview
El comando `getopts` en Bash se utiliza para analizar las opciones de línea de comandos en scripts. Permite a los desarrolladores manejar argumentos de manera estructurada, facilitando la creación de scripts más flexibles y fáciles de usar.

## Usage
La sintaxis básica del comando `getopts` es la siguiente:

```bash
getopts [options] [arguments]
```

## Common Options
- `-a`: Permite especificar opciones adicionales.
- `-o`: Define las opciones que se pueden utilizar.
- `-l`: Permite el uso de opciones largas.

## Common Examples

### Ejemplo 1: Análisis básico de opciones
```bash
#!/bin/bash

while getopts "ab:c" opt; do
  case $opt in
    a)
      echo "Opción A seleccionada"
      ;;
    b)
      echo "Opción B con argumento: $OPTARG"
      ;;
    c)
      echo "Opción C seleccionada"
      ;;
    *)
      echo "Opción no válida"
      ;;
  esac
done
```

### Ejemplo 2: Uso de opciones largas
```bash
#!/bin/bash

while getopts ":a:b:c" opt; do
  case $opt in
    a)
      echo "Opción A seleccionada"
      ;;
    b)
      echo "Opción B con argumento: $OPTARG"
      ;;
    c)
      echo "Opción C seleccionada"
      ;;
    *)
      echo "Opción no válida"
      ;;
  esac
done
```

### Ejemplo 3: Manejo de argumentos obligatorios
```bash
#!/bin/bash

while getopts ":a:b:" opt; do
  case $opt in
    a)
      echo "Opción A seleccionada con argumento: $OPTARG"
      ;;
    b)
      echo "Opción B seleccionada con argumento: $OPTARG"
      ;;
    *)
      echo "Opción no válida"
      ;;
  esac
done

if [ -z "$OPTARG" ]; then
  echo "Se requiere un argumento para la opción -a"
fi
```

## Tips
- Siempre verifica si los argumentos son válidos antes de procesarlos.
- Utiliza `OPTIND` para restablecer el índice de opciones si necesitas analizar múltiples conjuntos de opciones.
- Documenta las opciones que tu script acepta para que los usuarios puedan entender cómo utilizarlo correctamente.