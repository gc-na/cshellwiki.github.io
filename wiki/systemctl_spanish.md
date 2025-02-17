# [Linux] Bash systemctl uso: Gestión de servicios y unidades del sistema

## Overview
El comando `systemctl` es una herramienta de gestión para el sistema y los servicios en sistemas que utilizan `systemd` como sistema de inicialización. Permite a los usuarios iniciar, detener, reiniciar y verificar el estado de los servicios, así como gestionar otras unidades del sistema.

## Usage
La sintaxis básica del comando `systemctl` es la siguiente:

```bash
systemctl [opciones] [argumentos]
```

## Common Options
- `start`: Inicia una unidad o servicio.
- `stop`: Detiene una unidad o servicio.
- `restart`: Reinicia una unidad o servicio.
- `status`: Muestra el estado de una unidad o servicio.
- `enable`: Habilita una unidad para que se inicie automáticamente al arrancar el sistema.
- `disable`: Deshabilita una unidad para que no se inicie automáticamente al arrancar el sistema.
- `list-units`: Muestra una lista de todas las unidades activas.

## Common Examples
- Para iniciar un servicio, como `nginx`:
  ```bash
  systemctl start nginx
  ```

- Para detener un servicio, como `apache2`:
  ```bash
  systemctl stop apache2
  ```

- Para reiniciar un servicio, como `mysql`:
  ```bash
  systemctl restart mysql
  ```

- Para verificar el estado de un servicio, como `ssh`:
  ```bash
  systemctl status ssh
  ```

- Para habilitar un servicio para que se inicie al arrancar, como `cron`:
  ```bash
  systemctl enable cron
  ```

- Para deshabilitar un servicio para que no se inicie al arrancar, como `bluetooth`:
  ```bash
  systemctl disable bluetooth
  ```

- Para listar todas las unidades activas:
  ```bash
  systemctl list-units
  ```

## Tips
- Siempre verifica el estado de un servicio después de iniciar o detenerlo para asegurarte de que la acción se realizó correctamente.
- Utiliza `systemctl list-units --type=service` para filtrar y ver solo los servicios.
- Recuerda que algunas acciones pueden requerir privilegios de superusuario, así que considera usar `sudo` si encuentras problemas de permisos.