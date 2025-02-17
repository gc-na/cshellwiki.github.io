# [Linux] Bash gzip Uso: Comprimir y descomprimir archivos

## Overview
El comando `gzip` se utiliza para comprimir archivos en sistemas Unix y Linux. Su principal función es reducir el tamaño de los archivos, lo que facilita el almacenamiento y la transferencia de datos.

## Usage
La sintaxis básica del comando `gzip` es la siguiente:

```bash
gzip [opciones] [argumentos]
```

## Common Options
- `-d`, `--decompress`: Descomprime archivos.
- `-k`, `--keep`: Mantiene el archivo original después de la compresión.
- `-v`, `--verbose`: Muestra información detallada sobre el proceso de compresión.
- `-r`, `--recursive`: Comprime archivos en directorios de forma recursiva.

## Common Examples
1. **Comprimir un archivo:**
   ```bash
   gzip archivo.txt
   ```
   Esto creará un archivo comprimido llamado `archivo.txt.gz`.

2. **Descomprimir un archivo:**
   ```bash
   gzip -d archivo.txt.gz
   ```
   Esto restaurará el archivo original `archivo.txt`.

3. **Comprimir y mantener el archivo original:**
   ```bash
   gzip -k archivo.txt
   ```
   Esto generará `archivo.txt.gz` y mantendrá `archivo.txt`.

4. **Comprimir todos los archivos en un directorio:**
   ```bash
   gzip -r directorio/
   ```
   Esto comprimirá todos los archivos dentro de `directorio`.

5. **Ver información detallada durante la compresión:**
   ```bash
   gzip -v archivo.txt
   ```
   Esto mostrará el progreso de la compresión.

## Tips
- Utiliza la opción `-k` si deseas conservar los archivos originales después de la compresión.
- Para descomprimir múltiples archivos, puedes usar un patrón de búsqueda, como `gzip -d *.gz`.
- Recuerda que `gzip` solo puede comprimir archivos individuales; si necesitas comprimir directorios completos, considera usar `tar` junto con `gzip`.