# [Linux] Bash update-rc.d uso: Gestiona los scripts de inicio del sistema

## Overview
El comando `update-rc.d` se utiliza en sistemas basados en Debian para gestionar la instalación y eliminación de scripts de inicio en el directorio `/etc/rc.d`. Permite agregar o quitar scripts que se ejecutan automáticamente al iniciar o detener el sistema.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
update-rc.d [opciones] [argumentos]
```

## Common Options
- `defaults`: Instala el script con los niveles de ejecución predeterminados.
- `remove`: Elimina el script de los niveles de ejecución.
- `enable`: Activa el script en los niveles de ejecución especificados.
- `disable`: Desactiva el script en los niveles de ejecución especificados.

## Common Examples
1. **Instalar un script de inicio con valores predeterminados:**
   ```bash
   sudo update-rc.d mi-script defaults
   ```

2. **Eliminar un script de inicio:**
   ```bash
   sudo update-rc.d mi-script remove
   ```

3. **Activar un script en niveles de ejecución específicos:**
   ```bash
   sudo update-rc.d mi-script enable
   ```

4. **Desactivar un script en niveles de ejecución específicos:**
   ```bash
   sudo update-rc.d mi-script disable
   ```

## Tips
- Asegúrate de que tu script de inicio tenga los permisos de ejecución adecuados antes de usar `update-rc.d`.
- Siempre verifica los niveles de ejecución en los que deseas que se ejecute el script para evitar problemas en el arranque del sistema.
- Utiliza `update-rc.d -n` para simular la operación sin realizar cambios, lo que te permite verificar qué sucederá.