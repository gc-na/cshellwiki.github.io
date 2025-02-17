# [Linux] Bash xz Uso: Comprimir y descomprimir archivos

## Overview
El comando `xz` se utiliza para comprimir y descomprimir archivos utilizando el algoritmo de compresión LZMA. Es conocido por su alta tasa de compresión, lo que lo hace ideal para reducir el tamaño de archivos grandes.

## Usage
La sintaxis básica del comando `xz` es la siguiente:

```bash
xz [opciones] [argumentos]
```

## Common Options
- `-d`, `--decompress`: Descomprime el archivo.
- `-k`, `--keep`: Mantiene el archivo original después de la compresión.
- `-f`, `--force`: Fuerza la compresión o descompresión, sobrescribiendo archivos existentes.
- `-z`, `--compress`: Comprime el archivo (esta es la opción por defecto).
- `-9`: Utiliza el nivel de compresión más alto.

## Common Examples
### Comprimir un archivo
Para comprimir un archivo llamado `archivo.txt`, puedes usar el siguiente comando:

```bash
xz archivo.txt
```

### Descomprimir un archivo
Para descomprimir un archivo comprimido llamado `archivo.txt.xz`, utiliza:

```bash
xz -d archivo.txt.xz
```

### Mantener el archivo original
Si deseas comprimir un archivo pero mantener el original, puedes usar la opción `-k`:

```bash
xz -k archivo.txt
```

### Comprimir con el nivel más alto
Para comprimir un archivo utilizando el nivel de compresión más alto, puedes usar:

```bash
xz -9 archivo.txt
```

## Tips
- Siempre verifica el tamaño del archivo comprimido y descomprimido para asegurarte de que la compresión ha sido efectiva.
- Utiliza `-k` si no estás seguro de querer eliminar el archivo original después de la compresión.
- Considera usar `tar` junto con `xz` para comprimir directorios completos, ya que `xz` solo trabaja con archivos individuales.