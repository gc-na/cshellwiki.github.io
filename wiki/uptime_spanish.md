# [Linux] Bash uptime Uso equivalente en español: [muestra el tiempo de actividad del sistema]

## Overview
El comando `uptime` en Bash se utiliza para mostrar el tiempo que ha estado funcionando el sistema desde el último arranque. También proporciona información sobre el número de usuarios conectados y la carga promedio del sistema en los últimos 1, 5 y 15 minutos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
uptime [opciones]
```

## Common Options
- `-p`: Muestra el tiempo de actividad en un formato legible.
- `-s`: Muestra la hora y fecha del último arranque del sistema.

## Common Examples
A continuación se presentan algunos ejemplos prácticos del uso del comando `uptime`:

1. **Mostrar el tiempo de actividad del sistema:**
   ```bash
   uptime
   ```

2. **Mostrar el tiempo de actividad en un formato legible:**
   ```bash
   uptime -p
   ```

3. **Mostrar la fecha y hora del último arranque:**
   ```bash
   uptime -s
   ```

## Tips
- Utiliza `uptime` regularmente para monitorear la estabilidad de tu sistema.
- Combina `uptime` con otros comandos como `top` o `htop` para obtener una visión más completa del rendimiento del sistema.
- Si administras un servidor, considera programar `uptime` en un script de monitoreo para recibir alertas sobre el tiempo de actividad.