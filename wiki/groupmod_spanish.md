# [Linux] Bash groupmod uso: Modificar grupos en el sistema

## Overview
El comando `groupmod` se utiliza en sistemas Linux para modificar las propiedades de un grupo existente. Permite cambiar el nombre del grupo o su identificador (GID), facilitando la gestión de usuarios y grupos en el sistema.

## Usage
La sintaxis básica del comando es la siguiente:

```
groupmod [opciones] [argumentos]
```

## Common Options
- `-n, --new-name NOMBRE`: Cambia el nombre del grupo a NOMBRE.
- `-g, --gid GID`: Cambia el identificador del grupo a GID.
- `-h, --help`: Muestra la ayuda sobre el uso del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `groupmod`:

1. **Cambiar el nombre de un grupo:**
   ```bash
   groupmod -n nuevo_nombre viejo_nombre
   ```

2. **Cambiar el GID de un grupo:**
   ```bash
   groupmod -g 1001 nombre_del_grupo
   ```

3. **Modificar un grupo existente:**
   ```bash
   groupmod -n desarrolladores -g 2000 programadores
   ```

## Tips
- Asegúrate de que no haya usuarios conectados al grupo que estás modificando para evitar conflictos.
- Verifica los cambios utilizando el comando `getent group nombre_del_grupo` después de realizar modificaciones.
- Utiliza el comando `groupmod` con precaución, ya que cambiar el GID puede afectar a los permisos de archivos y directorios asociados.