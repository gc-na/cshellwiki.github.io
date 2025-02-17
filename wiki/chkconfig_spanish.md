# [Linux] Bash chkconfig uso: Gestionar servicios de inicio

## Overview
El comando `chkconfig` se utiliza en sistemas Linux para gestionar los servicios que se inician automáticamente durante el arranque del sistema. Permite habilitar o deshabilitar servicios en diferentes niveles de ejecución, facilitando la administración de los procesos que se ejecutan al inicio.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
chkconfig [opciones] [servicio] [acción]
```

## Common Options
- `--list`: Muestra el estado de todos los servicios y en qué niveles de ejecución están habilitados o deshabilitados.
- `--add`: Agrega un nuevo servicio al sistema de inicio.
- `--del`: Elimina un servicio del sistema de inicio.
- `--level`: Especifica los niveles de ejecución en los que se debe habilitar o deshabilitar el servicio.

## Common Examples
1. **Listar todos los servicios:**
   ```bash
   chkconfig --list
   ```

2. **Habilitar un servicio en todos los niveles de ejecución:**
   ```bash
   chkconfig nombre_del_servicio on
   ```

3. **Deshabilitar un servicio en todos los niveles de ejecución:**
   ```bash
   chkconfig nombre_del_servicio off
   ```

4. **Agregar un nuevo servicio:**
   ```bash
   chkconfig --add nombre_del_servicio
   ```

5. **Eliminar un servicio:**
   ```bash
   chkconfig --del nombre_del_servicio
   ```

## Tips
- Asegúrate de tener privilegios de superusuario (root) al utilizar `chkconfig`, ya que se requieren permisos elevados para modificar los servicios del sistema.
- Utiliza `chkconfig --list` regularmente para revisar el estado de los servicios y asegurarte de que solo los necesarios estén habilitados.
- Familiarízate con los niveles de ejecución de tu sistema, ya que esto te ayudará a gestionar mejor los servicios que deseas iniciar o detener.