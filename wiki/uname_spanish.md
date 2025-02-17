# [Linux] Bash uname Uso: Muestra información del sistema

## Overview
El comando `uname` se utiliza en sistemas Unix y Linux para mostrar información sobre el sistema operativo y el hardware en el que se está ejecutando. Es una herramienta útil para obtener detalles como el nombre del sistema, la versión del kernel y la arquitectura de la máquina.

## Usage
La sintaxis básica del comando `uname` es la siguiente:

```bash
uname [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas de las opciones más comunes que se pueden utilizar con el comando `uname`:

- `-a`: Muestra toda la información disponible sobre el sistema.
- `-s`: Muestra el nombre del sistema operativo.
- `-n`: Muestra el nombre del nodo de red (hostname).
- `-r`: Muestra la versión del kernel.
- `-v`: Muestra la fecha de compilación del kernel.
- `-m`: Muestra la arquitectura de la máquina.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `uname`:

1. Mostrar toda la información del sistema:
   ```bash
   uname -a
   ```

2. Mostrar solo el nombre del sistema operativo:
   ```bash
   uname -s
   ```

3. Mostrar el nombre del nodo de red:
   ```bash
   uname -n
   ```

4. Mostrar la versión del kernel:
   ```bash
   uname -r
   ```

5. Mostrar la arquitectura de la máquina:
   ```bash
   uname -m
   ```

## Tips
- Utiliza `uname -a` para obtener un resumen completo de la información del sistema en un solo comando.
- Puedes combinar `uname` con otros comandos, como `grep`, para filtrar la información que necesitas.
- Es útil ejecutar `uname` en scripts de inicio para registrar información del sistema en el que se está ejecutando el script.