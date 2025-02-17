# [Linux] Bash chgrp Uso: Cambiar el grupo de archivos y directorios

## Overview
El comando `chgrp` se utiliza en sistemas Unix y Linux para cambiar el grupo asociado a uno o más archivos o directorios. Esto es útil para gestionar permisos y accesos de usuarios en un entorno multiusuario.

## Usage
La sintaxis básica del comando `chgrp` es la siguiente:

```bash
chgrp [opciones] [grupo] [archivo/directorio]
```

## Common Options
- `-R`: Cambia el grupo de manera recursiva en todos los archivos y subdirectorios.
- `-v`: Muestra información detallada sobre los cambios realizados.
- `-c`: Muestra solo los archivos cuyos grupos han cambiado.

## Common Examples
1. Cambiar el grupo de un archivo:
   ```bash
   chgrp desarrolladores archivo.txt
   ```

2. Cambiar el grupo de un directorio:
   ```bash
   chgrp administradores /ruta/al/directorio
   ```

3. Cambiar el grupo de todos los archivos en un directorio de manera recursiva:
   ```bash
   chgrp -R usuarios /ruta/al/directorio
   ```

4. Cambiar el grupo de un archivo y mostrar los cambios:
   ```bash
   chgrp -v marketing informe.pdf
   ```

5. Cambiar el grupo de archivos específicos y mostrar solo los que han cambiado:
   ```bash
   chgrp -c contabilidad *.txt
   ```

## Tips
- Asegúrate de tener los permisos necesarios para cambiar el grupo de un archivo o directorio.
- Utiliza la opción `-R` con precaución, ya que puede afectar a muchos archivos y subdirectorios.
- Verifica el grupo actual de un archivo utilizando el comando `ls -l` antes de realizar cambios.