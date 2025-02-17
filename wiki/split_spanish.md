# [Linux] Bash split uso: Dividir archivos en partes más pequeñas

## Overview
El comando `split` en Bash se utiliza para dividir un archivo grande en varios archivos más pequeños. Esto es útil para manejar archivos que son demasiado grandes para ser procesados o transferidos de una sola vez.

## Usage
La sintaxis básica del comando `split` es la siguiente:

```bash
split [opciones] [archivo] [prefijo]
```

## Common Options
- `-l [n]`: Divide el archivo en partes de `n` líneas cada una.
- `-b [n]`: Divide el archivo en partes de `n` bytes cada una.
- `-d`: Usa números decimales en lugar de letras para nombrar los archivos resultantes.
- `--additional-suffix=[sufijo]`: Agrega un sufijo a los nombres de los archivos resultantes.

## Common Examples
1. Dividir un archivo en partes de 100 líneas cada una:
   ```bash
   split -l 100 archivo.txt
   ```

2. Dividir un archivo en partes de 1 MB cada una:
   ```bash
   split -b 1M archivo_grande.txt
   ```

3. Dividir un archivo y usar números decimales para los nombres de los archivos:
   ```bash
   split -d -l 50 archivo.txt parte_
   ```

4. Dividir un archivo y agregar un sufijo `.txt` a los nombres de los archivos resultantes:
   ```bash
   split --additional-suffix=.txt -l 10 archivo.txt parte_
   ```

## Tips
- Asegúrate de tener suficiente espacio en disco para almacenar los archivos resultantes.
- Utiliza el prefijo para organizar mejor los archivos divididos, especialmente si estás dividiendo múltiples archivos.
- Revisa el contenido de los archivos divididos para asegurarte de que la división se realizó correctamente. Puedes usar `cat` o `less` para visualizar los archivos.