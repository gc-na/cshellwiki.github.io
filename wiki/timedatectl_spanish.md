# [Linux] Bash timedatectl Uso: Gestión de la fecha y hora del sistema

## Overview
El comando `timedatectl` se utiliza para consultar y cambiar la configuración de la fecha y hora del sistema en sistemas operativos basados en Linux. Permite a los usuarios gestionar la sincronización del tiempo y la zona horaria de manera sencilla.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
timedatectl [opciones] [argumentos]
```

## Common Options
- `set-time`: Establece la fecha y hora del sistema.
- `set-timezone`: Cambia la zona horaria del sistema.
- `status`: Muestra la fecha, hora, zona horaria y estado de sincronización.
- `list-timezones`: Lista todas las zonas horarias disponibles.
- `set-ntp`: Habilita o deshabilita la sincronización automática del tiempo a través de NTP (Network Time Protocol).

## Common Examples
- **Mostrar el estado actual de la fecha y hora:**

```bash
timedatectl status
```

- **Establecer la fecha y hora manualmente:**

```bash
timedatectl set-time '2023-10-01 12:00:00'
```

- **Cambiar la zona horaria a Europa/Madrid:**

```bash
timedatectl set-timezone Europe/Madrid
```

- **Listar todas las zonas horarias disponibles:**

```bash
timedatectl list-timezones
```

- **Habilitar la sincronización NTP:**

```bash
timedatectl set-ntp true
```

## Tips
- Asegúrate de tener privilegios de administrador (root) para realizar cambios en la configuración de la fecha y hora.
- Utiliza `timedatectl list-timezones` para encontrar la zona horaria correcta antes de cambiarla.
- Verifica regularmente el estado del tiempo del sistema, especialmente si dependes de aplicaciones que requieren una hora precisa.