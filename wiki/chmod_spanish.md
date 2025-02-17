# [Linux] Bash chmod uso: Cambiar permisos de archivos y directorios

## Overview
El comando `chmod` se utiliza en sistemas Unix y Linux para cambiar los permisos de acceso a archivos y directorios. Permite a los usuarios definir quién puede leer, escribir o ejecutar un archivo.

## Usage
La sintaxis básica del comando `chmod` es la siguiente:

```bash
chmod [opciones] [argumentos]
```

## Common Options
- `-R`: Aplica los cambios de permisos de manera recursiva a todos los archivos y subdirectorios.
- `-v`: Muestra información detallada sobre los cambios realizados.
- `-c`: Muestra solo los archivos cuyos permisos han cambiado.

## Common Examples
1. **Cambiar permisos a un archivo específico:**
   Para dar permisos de lectura y escritura al propietario y solo lectura a los demás:
   ```bash
   chmod 644 archivo.txt
   ```

2. **Dar permisos de ejecución a un script:**
   Para permitir que todos los usuarios puedan ejecutar un script:
   ```bash
   chmod +x script.sh
   ```

3. **Cambiar permisos de manera recursiva:**
   Para dar permisos de lectura, escritura y ejecución al propietario y solo lectura a los demás en un directorio y su contenido:
   ```bash
   chmod -R 755 directorio/
   ```

4. **Eliminar permisos:**
   Para quitar el permiso de escritura a otros usuarios en un archivo:
   ```bash
   chmod o-w archivo.txt
   ```

## Tips
- Siempre verifica los permisos actuales de un archivo con `ls -l` antes de realizar cambios.
- Utiliza la opción `-v` para ver qué cambios se están aplicando, especialmente cuando trabajas con múltiples archivos.
- Ten cuidado al usar la opción `-R`, ya que puede cambiar permisos en muchos archivos y directorios de una sola vez.