# [Linux] Bash od: [visualizar archivos en formato hexadecimal y octal]

## Overview
El comando `od` (octal dump) se utiliza para mostrar el contenido de archivos en diferentes formatos, como octal, hexadecimal, decimal y caracteres ASCII. Es especialmente útil para analizar archivos binarios y ver su representación en diferentes bases numéricas.

## Usage
La sintaxis básica del comando es la siguiente:

```
od [opciones] [argumentos]
```

## Common Options
- `-A, --address-radix=RADIX`: Especifica el formato de la dirección (octal, decimal, hexadecimal).
- `-t, --format=TYPE`: Define el tipo de salida, como octal (`o`), hexadecimal (`x`), decimal (`d`), etc.
- `-N, --read-bytes=N`: Lee solo N bytes del archivo.
- `-v, --output-duplicates`: Muestra todos los datos, incluso los duplicados.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `od`:

1. **Mostrar el contenido de un archivo en formato octal:**
   ```bash
   od -o archivo.txt
   ```

2. **Mostrar el contenido en formato hexadecimal:**
   ```bash
   od -x archivo.bin
   ```

3. **Leer solo los primeros 16 bytes de un archivo:**
   ```bash
   od -N 16 archivo.txt
   ```

4. **Mostrar el contenido en formato decimal:**
   ```bash
   od -d archivo.bin
   ```

5. **Combinar varios formatos en una sola salida:**
   ```bash
   od -t x1 -t c archivo.txt
   ```

## Tips
- Utiliza la opción `-A` para cambiar el formato de las direcciones y facilitar la lectura de los datos.
- Experimenta con diferentes formatos usando `-t` para encontrar el que mejor se adapte a tus necesidades.
- Recuerda que `od` es más útil para archivos binarios, así que asegúrate de que el archivo que estás analizando sea adecuado para este comando.