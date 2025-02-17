# [Linux] Bash iconv uso: Conversión de codificaciones de texto

## Overview
El comando `iconv` se utiliza para convertir la codificación de caracteres de archivos de texto. Es especialmente útil cuando se trabaja con archivos que contienen caracteres especiales o cuando se necesita cambiar la codificación para cumplir con requisitos específicos de software o sistemas.

## Usage
La sintaxis básica del comando `iconv` es la siguiente:

```bash
iconv [opciones] [argumentos]
```

## Common Options
- `-f, --from-code=CODIGO`: Especifica la codificación de entrada.
- `-t, --to-code=CODIGO`: Especifica la codificación de salida.
- `-o, --output=ARCHIVO`: Redirige la salida a un archivo en lugar de la salida estándar.
- `-c`: Omite los caracteres que no se pueden convertir.

## Common Examples

1. **Convertir un archivo de UTF-8 a ISO-8859-1:**
   ```bash
   iconv -f UTF-8 -t ISO-8859-1 archivo_entrada.txt -o archivo_salida.txt
   ```

2. **Convertir un archivo de Windows-1252 a UTF-8:**
   ```bash
   iconv -f WINDOWS-1252 -t UTF-8 archivo_entrada.txt -o archivo_salida.txt
   ```

3. **Convertir y mostrar el resultado en la consola:**
   ```bash
   iconv -f UTF-8 -t ASCII//TRANSLIT archivo_entrada.txt
   ```

4. **Eliminar caracteres no convertibles:**
   ```bash
   iconv -f UTF-8 -t ISO-8859-1//IGNORE archivo_entrada.txt -o archivo_salida.txt
   ```

## Tips
- Siempre verifica la codificación de los archivos de entrada antes de realizar la conversión para evitar pérdida de datos.
- Utiliza la opción `-o` para guardar los resultados en un nuevo archivo y así preservar el archivo original.
- Si no estás seguro de las codificaciones disponibles, puedes usar `iconv -l` para listar todas las codificaciones soportadas.