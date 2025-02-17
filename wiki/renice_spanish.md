# [Linux] Bash renice uso equivalente: Cambiar la prioridad de un proceso

## Overview
El comando `renice` se utiliza en sistemas Unix y Linux para cambiar la prioridad de ejecución de uno o más procesos en ejecución. La prioridad determina la cantidad de tiempo de CPU que un proceso puede utilizar; un número más bajo indica una mayor prioridad.

## Usage
La sintaxis básica del comando `renice` es la siguiente:

```bash
renice [opciones] [argumentos]
```

## Common Options
- `-n, --priority <n>`: Establece la nueva prioridad para el proceso. Los valores pueden ser negativos (mayor prioridad) o positivos (menor prioridad).
- `-p, --pid <pid>`: Especifica el ID del proceso al que se le cambiará la prioridad.
- `-g, --pgrp <pgrp>`: Cambia la prioridad de todos los procesos en el grupo de procesos especificado.
- `-u, --user <usuario>`: Cambia la prioridad de todos los procesos del usuario especificado.

## Common Examples
1. Cambiar la prioridad de un proceso específico:
   ```bash
   renice -n 10 -p 1234
   ```
   Este comando establece la prioridad del proceso con ID 1234 a 10.

2. Cambiar la prioridad de todos los procesos de un usuario:
   ```bash
   renice -n -5 -u usuario
   ```
   Aquí, todos los procesos del usuario "usuario" se establecen con una prioridad de -5.

3. Cambiar la prioridad de un grupo de procesos:
   ```bash
   renice -n 15 -g 5678
   ```
   Este comando cambia la prioridad de todos los procesos en el grupo de procesos con ID 5678 a 15.

## Tips
- Utiliza `renice` con precaución, ya que establecer prioridades muy altas o bajas puede afectar el rendimiento del sistema.
- Puedes verificar la prioridad actual de un proceso usando el comando `ps` antes de aplicar `renice`.
- Asegúrate de tener los permisos necesarios para cambiar la prioridad de los procesos, especialmente si no son de tu propiedad.