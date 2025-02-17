# [Linux] Bash rm Uso: Eliminar archivos y directorios

## Overview
El comando `rm` se utiliza en sistemas Unix y Linux para eliminar archivos y directorios. Es una herramienta poderosa que permite borrar datos de manera permanente, así que se debe usar con precaución.

## Usage
La sintaxis básica del comando `rm` es la siguiente:

```
rm [opciones] [argumentos]
```

## Common Options
- `-f`: Fuerza la eliminación sin pedir confirmación.
- `-i`: Pide confirmación antes de eliminar cada archivo.
- `-r`: Elimina directorios y su contenido de manera recursiva.
- `-v`: Muestra información detallada sobre lo que se está eliminando.

## Common Examples
- Eliminar un solo archivo:
  ```bash
  rm archivo.txt
  ```

- Eliminar varios archivos:
  ```bash
  rm archivo1.txt archivo2.txt archivo3.txt
  ```

- Eliminar un directorio y su contenido de forma recursiva:
  ```bash
  rm -r directorio/
  ```

- Forzar la eliminación sin confirmación:
  ```bash
  rm -f archivo.txt
  ```

- Pedir confirmación antes de eliminar:
  ```bash
  rm -i archivo.txt
  ```

## Tips
- Siempre verifica el nombre del archivo o directorio antes de usar `rm`, especialmente con la opción `-f`.
- Considera usar `rm -i` si no estás seguro de lo que estás eliminando.
- Para evitar eliminar archivos accidentalmente, puedes usar `mv` para mover los archivos a una ubicación temporal antes de eliminarlos.