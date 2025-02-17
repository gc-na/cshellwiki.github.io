# [Linux] Bash tail uso: Muestra las últimas líneas de un archivo

## Overview
El comando `tail` se utiliza en Bash para mostrar las últimas líneas de un archivo de texto. Es especialmente útil para monitorear archivos de registro en tiempo real o para ver la parte final de archivos grandes sin necesidad de abrirlos completamente.

## Usage
La sintaxis básica del comando `tail` es la siguiente:

```bash
tail [opciones] [archivo]
```

## Common Options
- `-n [número]`: Muestra las últimas `n` líneas del archivo. Por defecto, muestra 10 líneas.
- `-f`: Sigue el archivo en tiempo real, mostrando nuevas líneas a medida que se agregan.
- `-c [número]`: Muestra los últimos `n` bytes del archivo.
- `-q`: Suprime la salida del encabezado de los archivos cuando se utilizan múltiples archivos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `tail`:

1. Mostrar las últimas 20 líneas de un archivo:
   ```bash
   tail -n 20 archivo.txt
   ```

2. Seguir un archivo de registro en tiempo real:
   ```bash
   tail -f /var/log/syslog
   ```

3. Mostrar los últimos 100 bytes de un archivo:
   ```bash
   tail -c 100 archivo.txt
   ```

4. Mostrar las últimas líneas de varios archivos:
   ```bash
   tail -n 10 archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza `tail -f` para monitorear archivos de registro en tiempo real, lo que es útil para depurar aplicaciones.
- Combina `tail` con otros comandos como `grep` para filtrar la salida. Por ejemplo:
  ```bash
  tail -f archivo.log | grep "ERROR"
  ```
- Si necesitas ver las últimas líneas de un archivo que se está escribiendo, `tail -f` es tu mejor opción, ya que actualizará automáticamente la salida.