# [Linux] Bash iostat Uso: Monitoreo del rendimiento de entrada/salida

## Overview
El comando `iostat` se utiliza para monitorear el rendimiento de entrada/salida de los dispositivos de almacenamiento y las particiones en un sistema Linux. Proporciona estadísticas sobre la utilización de la CPU y el rendimiento de los dispositivos de bloque, lo que ayuda a identificar cuellos de botella en el sistema.

## Usage
La sintaxis básica del comando `iostat` es la siguiente:

```bash
iostat [opciones] [argumentos]
```

## Common Options
- `-c`: Muestra estadísticas de la CPU.
- `-d`: Muestra estadísticas de los dispositivos de bloque.
- `-x`: Proporciona estadísticas extendidas de los dispositivos.
- `-m`: Muestra los resultados en megabytes por segundo.
- `-t`: Muestra la hora y la fecha en la salida.

## Common Examples
1. **Mostrar estadísticas de CPU y dispositivos de bloque:**
   ```bash
   iostat
   ```

2. **Mostrar solo estadísticas de CPU:**
   ```bash
   iostat -c
   ```

3. **Mostrar estadísticas de dispositivos de bloque con detalles extendidos:**
   ```bash
   iostat -dx
   ```

4. **Mostrar estadísticas en megabytes por segundo:**
   ```bash
   iostat -m
   ```

5. **Monitorear cada 5 segundos:**
   ```bash
   iostat 5
   ```

## Tips
- Utiliza `iostat` junto con otros comandos como `vmstat` y `mpstat` para obtener una visión más completa del rendimiento del sistema.
- Revisa las estadísticas de iostat durante períodos de alta carga para identificar posibles problemas de rendimiento.
- Considera redirigir la salida a un archivo para análisis posterior, usando `iostat -x 5 > salida.txt`.