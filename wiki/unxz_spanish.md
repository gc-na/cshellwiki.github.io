# [Linux] Bash unxz uso: Descomprimir archivos .xz

## Overview
El comando `unxz` se utiliza para descomprimir archivos que han sido comprimidos con el algoritmo XZ. Este comando es parte de la suite de herramientas XZ Utils y permite recuperar el archivo original a partir de su versión comprimida.

## Usage
La sintaxis básica del comando `unxz` es la siguiente:

```
unxz [opciones] [argumentos]
```

## Common Options
- `-k`, `--keep`: Mantiene el archivo comprimido después de descomprimirlo.
- `-f`, `--force`: Fuerza la descompresión, sobrescribiendo archivos existentes sin pedir confirmación.
- `-v`, `--verbose`: Muestra información detallada sobre el proceso de descompresión.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `unxz`:

1. **Descomprimir un archivo .xz**:
   ```bash
   unxz archivo.xz
   ```

2. **Descomprimir y mantener el archivo original**:
   ```bash
   unxz -k archivo.xz
   ```

3. **Forzar la descompresión, sobrescribiendo archivos existentes**:
   ```bash
   unxz -f archivo.xz
   ```

4. **Descomprimir un archivo y mostrar el proceso**:
   ```bash
   unxz -v archivo.xz
   ```

## Tips
- Asegúrate de tener suficiente espacio en disco antes de descomprimir archivos grandes.
- Si necesitas descomprimir múltiples archivos a la vez, puedes usar un comodín:
  ```bash
  unxz *.xz
  ```
- Siempre verifica el archivo descomprimido para asegurarte de que no esté corrupto, especialmente si fue descargado de Internet.