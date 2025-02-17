# [Linux] Bash time uso equivalente: mide el tiempo de ejecución de comandos

## Overview
El comando `time` en Bash se utiliza para medir el tiempo que tarda en ejecutarse un comando o un script. Proporciona información sobre el tiempo real, el tiempo de CPU utilizado y otros detalles que pueden ser útiles para optimizar el rendimiento de los scripts.

## Usage
La sintaxis básica del comando `time` es la siguiente:

```bash
time [opciones] [argumentos]
```

## Common Options
- `-p`: Muestra el tiempo en un formato más legible y estándar.
- `-o archivo`: Redirige la salida del tiempo a un archivo especificado.
- `-v`: Muestra información detallada sobre el uso de recursos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `time`:

1. Medir el tiempo de ejecución de un comando simple:
   ```bash
   time ls -l
   ```

2. Guardar la salida del tiempo en un archivo:
   ```bash
   time -o tiempo.txt sleep 2
   ```

3. Usar el formato de salida estándar:
   ```bash
   time -p sleep 3
   ```

4. Obtener información detallada sobre el uso de recursos:
   ```bash
   /usr/bin/time -v find / -name "*.txt"
   ```

## Tips
- Utiliza `time` para identificar cuellos de botella en tus scripts y optimizar su rendimiento.
- Recuerda que `time` mide solo el tiempo de ejecución del comando especificado, no incluye el tiempo de preparación o de otros procesos.
- Puedes combinar `time` con otros comandos en una tubería para medir el tiempo de ejecución de procesos más complejos.