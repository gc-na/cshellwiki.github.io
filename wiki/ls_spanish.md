# [Linux] Bash ls Uso equivalente: listar archivos y directorios

## Overview
El comando `ls` se utiliza en sistemas Unix y Linux para listar los archivos y directorios en un directorio específico. Es una herramienta fundamental para navegar y gestionar el sistema de archivos.

## Usage
La sintaxis básica del comando `ls` es la siguiente:

```bash
ls [opciones] [argumentos]
```

## Common Options
Aquí hay algunas opciones comunes que se pueden usar con el comando `ls`:

- `-l`: Muestra la lista en formato largo, incluyendo permisos, propietario, tamaño y fecha de modificación.
- `-a`: Muestra todos los archivos, incluidos los ocultos (que comienzan con un punto).
- `-h`: Muestra los tamaños de archivo en un formato legible para humanos (por ejemplo, KB, MB).
- `-R`: Lista los directorios de forma recursiva.
- `-t`: Ordena los archivos por fecha de modificación, mostrando primero los más recientes.

## Common Examples
A continuación se presentan algunos ejemplos prácticos del uso del comando `ls`:

1. Listar archivos en el directorio actual:
   ```bash
   ls
   ```

2. Listar archivos con detalles en formato largo:
   ```bash
   ls -l
   ```

3. Listar todos los archivos, incluidos los ocultos:
   ```bash
   ls -a
   ```

4. Listar archivos con tamaños legibles para humanos:
   ```bash
   ls -lh
   ```

5. Listar archivos de forma recursiva en todos los subdirectorios:
   ```bash
   ls -R
   ```

6. Listar archivos ordenados por fecha de modificación:
   ```bash
   ls -lt
   ```

## Tips
- Combina opciones para obtener la salida deseada, por ejemplo, `ls -la` para ver todos los archivos en formato largo.
- Utiliza `ls` junto con tuberías para filtrar resultados, como `ls -l | grep "txt"` para listar solo archivos de texto.
- Recuerda que el orden de las opciones no afecta el resultado, puedes escribir `ls -al` o `ls -la` indistintamente.