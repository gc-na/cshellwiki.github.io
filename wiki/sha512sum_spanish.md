# [Linux] Bash sha512sum uso: Calcular y verificar sumas de verificación SHA-512

## Overview
El comando `sha512sum` se utiliza para calcular y verificar sumas de verificación SHA-512 de archivos. Esto es útil para comprobar la integridad de los datos, asegurando que un archivo no ha sido alterado.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
sha512sum [opciones] [argumentos]
```

## Common Options
- `-b`: Procesa el archivo como un archivo binario.
- `-c`: Verifica las sumas de verificación en un archivo de suma de verificación.
- `--quiet`: No muestra el nombre del archivo durante la verificación.
- `--tag`: Produce una salida en formato de etiqueta.

## Common Examples

### Calcular la suma de verificación de un archivo
Para calcular la suma de verificación SHA-512 de un archivo llamado `archivo.txt`, puedes usar:

```bash
sha512sum archivo.txt
```

### Verificar sumas de verificación desde un archivo
Si tienes un archivo llamado `sumas.txt` que contiene sumas de verificación y nombres de archivos, puedes verificar los archivos con:

```bash
sha512sum -c sumas.txt
```

### Calcular la suma de verificación de varios archivos
Para calcular las sumas de verificación de varios archivos a la vez, simplemente enumera los archivos:

```bash
sha512sum archivo1.txt archivo2.txt archivo3.txt
```

### Usar la opción de archivo binario
Si deseas calcular la suma de un archivo binario, puedes usar la opción `-b`:

```bash
sha512sum -b archivo.bin
```

## Tips
- Siempre verifica las sumas de verificación después de transferir archivos importantes para asegurarte de que no se hayan corrompido.
- Guarda las sumas de verificación en un archivo separado para facilitar la verificación futura.
- Utiliza la opción `--quiet` si solo deseas ver el resultado de la verificación sin los nombres de los archivos.