# [Linux] Bash head Uso: Muestra las primeras líneas de un archivo

## Overview
El comando `head` en Bash se utiliza para mostrar las primeras líneas de uno o más archivos de texto. Es especialmente útil para obtener una vista rápida del contenido de un archivo sin necesidad de abrirlo completamente.

## Usage
La sintaxis básica del comando `head` es la siguiente:

```bash
head [opciones] [archivo]
```

## Common Options
- `-n [número]`: Especifica el número de líneas que se mostrarán. Por defecto, muestra las primeras 10 líneas.
- `-c [número]`: Muestra el número especificado de bytes del archivo.
- `-q`: Suprime la impresión de los nombres de los archivos cuando se muestran múltiples archivos.
- `-v`: Muestra el nombre del archivo antes de las líneas que se están mostrando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `head`:

1. Mostrar las primeras 10 líneas de un archivo:
   ```bash
   head archivo.txt
   ```

2. Mostrar las primeras 5 líneas de un archivo:
   ```bash
   head -n 5 archivo.txt
   ```

3. Mostrar los primeros 20 bytes de un archivo:
   ```bash
   head -c 20 archivo.txt
   ```

4. Mostrar las primeras 10 líneas de múltiples archivos:
   ```bash
   head archivo1.txt archivo2.txt
   ```

5. Mostrar las primeras 10 líneas de un archivo sin mostrar el nombre del archivo:
   ```bash
   head -q archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza `head` junto con otros comandos mediante tuberías para filtrar la salida. Por ejemplo, `ls -l | head` mostrará las primeras 10 entradas de un listado detallado.
- Si necesitas ver las últimas líneas de un archivo, considera usar el comando `tail`, que está diseñado para esa función.
- Recuerda que `head` puede ser muy útil en scripts para verificar rápidamente el contenido de archivos generados o logs.