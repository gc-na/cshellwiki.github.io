# [Linux] Bash 7z Uso: Comprimir y descomprimir archivos

## Overview
El comando `7z` es una herramienta de línea de comandos utilizada para comprimir y descomprimir archivos y directorios. Es parte del software 7-Zip, que es conocido por su alta tasa de compresión y soporte para varios formatos de archivo.

## Usage
La sintaxis básica del comando `7z` es la siguiente:

```
7z [opciones] [argumentos]
```

## Common Options
- `a`: Añadir archivos a un archivo comprimido.
- `x`: Extraer archivos de un archivo comprimido.
- `l`: Listar el contenido de un archivo comprimido.
- `d`: Eliminar archivos de un archivo comprimido.
- `t`: Especificar el tipo de archivo (por ejemplo, `zip`, `7z`).

## Common Examples
### Comprimir un archivo
Para comprimir un archivo llamado `documento.txt` en un archivo `documento.7z`, puedes usar el siguiente comando:

```
7z a documento.7z documento.txt
```

### Descomprimir un archivo
Para extraer el contenido de `documento.7z`, utiliza:

```
7z x documento.7z
```

### Listar el contenido de un archivo comprimido
Para ver qué archivos están dentro de `documento.7z`, ejecuta:

```
7z l documento.7z
```

### Eliminar un archivo de un archivo comprimido
Si deseas eliminar `documento.txt` de `documento.7z`, puedes hacerlo con:

```
7z d documento.7z documento.txt
```

## Tips
- Siempre verifica el contenido de un archivo comprimido con `l` antes de extraerlo para asegurarte de que contiene lo que esperas.
- Usa la opción `-p` para establecer una contraseña al crear un archivo comprimido, lo que añade una capa de seguridad.
- Para comprimir varios archivos a la vez, simplemente enumera los archivos después del nombre del archivo comprimido, por ejemplo: `7z a archivo.7z archivo1.txt archivo2.txt`.