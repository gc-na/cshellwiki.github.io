# [Linux] Bash killall Uso: Termina procesos por nombre

## Overview
El comando `killall` se utiliza en sistemas Unix y Linux para terminar procesos en ejecución basándose en su nombre. A diferencia de otros comandos de terminación de procesos, `killall` permite especificar el nombre del proceso que se desea finalizar, lo que facilita la gestión de múltiples instancias de un mismo programa.

## Usage
La sintaxis básica del comando `killall` es la siguiente:

```bash
killall [opciones] [nombre_del_proceso]
```

## Common Options
- `-u, --user <usuario>`: Termina los procesos que pertenecen a un usuario específico.
- `-i, --interactive`: Solicita confirmación antes de terminar cada proceso.
- `-q, --quiet`: No muestra mensajes de error si no se encuentran procesos.
- `-v, --verbose`: Muestra información detallada sobre los procesos que se están terminando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `killall`:

1. Terminar todos los procesos de Firefox:
   ```bash
   killall firefox
   ```

2. Terminar todos los procesos de un usuario específico:
   ```bash
   killall -u nombre_usuario
   ```

3. Terminar un proceso y solicitar confirmación:
   ```bash
   killall -i nombre_del_proceso
   ```

4. Terminar todos los procesos de un programa y mostrar información detallada:
   ```bash
   killall -v nombre_del_proceso
   ```

## Tips
- Asegúrate de tener los permisos necesarios para terminar procesos que no son de tu propiedad.
- Utiliza la opción `-i` si no estás seguro de qué procesos se van a terminar, para evitar cerrar accidentalmente procesos importantes.
- Puedes combinar `killall` con otros comandos, como `ps`, para listar procesos antes de decidir cuáles terminar.