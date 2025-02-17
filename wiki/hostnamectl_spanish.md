# [Linux] Bash hostnamectl Uso: Gestión de nombres de host del sistema

El comando `hostnamectl` se utiliza para consultar y cambiar el nombre de host del sistema en sistemas que utilizan systemd.

## Overview
El comando `hostnamectl` permite a los usuarios gestionar el nombre de host de su sistema, así como obtener información sobre el estado actual del sistema. Esto incluye el nombre de host estático, el nombre de host transitorio y el nombre de host de la red.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
hostnamectl [opciones] [argumentos]
```

## Common Options
- `set-hostname`: Cambia el nombre de host del sistema.
- `status`: Muestra el estado actual del nombre de host y otra información del sistema.
- `set-icon-name`: Establece un nombre de icono para el sistema.
- `set-chassis`: Define el tipo de chasis del sistema (por ejemplo, desktop, laptop, etc.).

## Common Examples
1. **Ver el estado actual del sistema:**
   ```bash
   hostnamectl status
   ```

2. **Cambiar el nombre de host estático:**
   ```bash
   sudo hostnamectl set-hostname nuevo-nombre-host
   ```

3. **Establecer un nombre de icono:**
   ```bash
   sudo hostnamectl set-icon-name computadora
   ```

4. **Definir el tipo de chasis:**
   ```bash
   sudo hostnamectl set-chassis laptop
   ```

## Tips
- Asegúrate de tener privilegios de superusuario (sudo) al cambiar el nombre de host.
- Después de cambiar el nombre de host, es recomendable reiniciar el sistema para que todos los servicios reconozcan el nuevo nombre.
- Utiliza `hostnamectl status` para verificar que los cambios se hayan aplicado correctamente.