# [Linux] Bash cksum Uso: Calcular el valor de verificación de archivos

## Overview
El comando `cksum` se utiliza para calcular y mostrar el valor de verificación (checksum) de un archivo, así como su tamaño en bytes. Este valor es útil para verificar la integridad de los archivos, ya que cualquier cambio en el contenido del archivo resultará en un valor de verificación diferente.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
cksum [opciones] [archivos]
```

## Common Options
- `-a, --algorithm=ALGORITMO`: Especifica el algoritmo a utilizar para calcular el checksum.
- `--help`: Muestra la ayuda sobre el comando y sus opciones.
- `--version`: Muestra la versión del comando `cksum`.

## Common Examples

1. **Calcular el checksum de un archivo:**
   ```bash
   cksum archivo.txt
   ```

2. **Calcular el checksum de varios archivos:**
   ```bash
   cksum archivo1.txt archivo2.txt
   ```

3. **Usar una opción para mostrar la ayuda:**
   ```bash
   cksum --help
   ```

4. **Calcular el checksum de un archivo y redirigir la salida a un archivo:**
   ```bash
   cksum archivo.txt > checksum.txt
   ```

## Tips
- Asegúrate de tener permisos de lectura en los archivos que deseas verificar.
- Utiliza `cksum` junto con otros comandos como `diff` para comparar archivos.
- Guarda el valor de verificación en un archivo para futuras comparaciones y verificar la integridad de los archivos a lo largo del tiempo.