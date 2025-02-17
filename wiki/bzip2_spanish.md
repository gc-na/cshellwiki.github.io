# [Linux] Bash bzip2 Uso: Comprimir y descomprimir archivos

## Overview
El comando `bzip2` se utiliza para comprimir archivos en sistemas Unix y Linux. Genera archivos con la extensión `.bz2`, que son más pequeños que los archivos originales, facilitando su almacenamiento y transferencia.

## Usage
La sintaxis básica del comando `bzip2` es la siguiente:

```bash
bzip2 [opciones] [argumentos]
```

## Common Options
- `-d`, `--decompress`: Descomprime un archivo `.bz2`.
- `-k`, `--keep`: Mantiene el archivo original después de la compresión.
- `-f`, `--force`: Fuerza la compresión o descompresión, sobrescribiendo archivos existentes.
- `-v`, `--verbose`: Muestra información detallada sobre el proceso de compresión o descompresión.
- `-z`, `--compress`: Comprime el archivo (comportamiento predeterminado).

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `bzip2`:

1. **Comprimir un archivo**:
   ```bash
   bzip2 archivo.txt
   ```
   Esto creará un archivo llamado `archivo.txt.bz2` y eliminará el archivo original.

2. **Descomprimir un archivo**:
   ```bash
   bzip2 -d archivo.txt.bz2
   ```
   Esto restaurará el archivo original `archivo.txt` y eliminará el archivo comprimido.

3. **Mantener el archivo original al comprimir**:
   ```bash
   bzip2 -k archivo.txt
   ```
   Esto creará `archivo.txt.bz2` pero mantendrá `archivo.txt` intacto.

4. **Comprimir múltiples archivos**:
   ```bash
   bzip2 archivo1.txt archivo2.txt
   ```
   Esto comprimirá ambos archivos y generará `archivo1.txt.bz2` y `archivo2.txt.bz2`.

5. **Ver información detallada durante la compresión**:
   ```bash
   bzip2 -v archivo.txt
   ```
   Esto mostrará información sobre el proceso de compresión.

## Tips
- Siempre verifica el espacio en disco antes de comprimir archivos grandes, ya que el proceso puede requerir espacio adicional temporal.
- Utiliza la opción `-k` si deseas mantener los archivos originales, especialmente cuando estás probando la compresión.
- Para descomprimir archivos en un script, considera usar `bzip2 -d` para evitar la eliminación accidental de archivos comprimidos.