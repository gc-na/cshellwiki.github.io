# [Linux] Bash nice uso: Controlar la prioridad de los procesos

## Overview
El comando `nice` se utiliza en sistemas Unix y Linux para ejecutar un programa con una prioridad de CPU ajustada. Permite que los usuarios modifiquen la prioridad de un proceso, lo que puede ser útil para gestionar la carga del sistema y asegurar que los procesos más importantes reciban más recursos de CPU.

## Usage
La sintaxis básica del comando `nice` es la siguiente:

```
nice [opciones] [comando]
```

## Common Options
- `-n, --adjustment=N`: Establece el valor de ajuste de la prioridad. Puede ser un número positivo o negativo.
- `--help`: Muestra la ayuda sobre el comando.
- `--version`: Muestra la versión del comando.

## Common Examples
1. Ejecutar un comando con una prioridad más baja:
   ```bash
   nice -n 10 myscript.sh
   ```

2. Ejecutar un comando con una prioridad más alta:
   ```bash
   nice -n -5 myscript.sh
   ```

3. Verificar la prioridad de un proceso en ejecución:
   ```bash
   ps -o pid,ni,cmd
   ```

4. Ejecutar un comando en segundo plano con prioridad ajustada:
   ```bash
   nice -n 15 long_running_task &
   ```

## Tips
- Utiliza valores negativos con precaución, ya que pueden afectar el rendimiento de otros procesos en el sistema.
- Para ver la prioridad de los procesos en ejecución, puedes usar el comando `ps` junto con `nice`.
- Recuerda que solo el usuario root puede establecer prioridades negativas para los procesos.