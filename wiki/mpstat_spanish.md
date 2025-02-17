# [Linux] Bash mpstat Uso: Monitoreo del rendimiento de la CPU

## Overview
El comando `mpstat` se utiliza para mostrar estadísticas de uso de la CPU en sistemas Linux. Permite a los usuarios obtener información detallada sobre el rendimiento de cada núcleo de la CPU, lo que es útil para identificar cuellos de botella y optimizar el rendimiento del sistema.

## Usage
La sintaxis básica del comando `mpstat` es la siguiente:

```bash
mpstat [opciones] [intervalo] [número de repeticiones]
```

## Common Options
- `-P ALL`: Muestra estadísticas para todas las CPUs.
- `-u`: Muestra el uso de la CPU en porcentaje.
- `-h`: Muestra la salida en un formato más legible (human-readable).
- `-o`: Especifica el formato de salida (por ejemplo, CSV).
- `-V`: Muestra la versión del comando.

## Common Examples
1. **Mostrar estadísticas de todas las CPUs cada 2 segundos:**

   ```bash
   mpstat -P ALL 2
   ```

2. **Mostrar el uso de la CPU en un formato legible:**

   ```bash
   mpstat -u -h 1 5
   ```

3. **Guardar la salida en formato CSV:**

   ```bash
   mpstat -P ALL -o CSV 1 10 > estadisticas_cpu.csv
   ```

4. **Mostrar estadísticas de la CPU 0 cada 5 segundos:**

   ```bash
   mpstat -P 0 5
   ```

## Tips
- Utiliza `mpstat -P ALL` para tener una visión completa del rendimiento de cada núcleo de la CPU.
- Combina `mpstat` con otras herramientas como `grep` para filtrar información específica.
- Considera usar `-h` para facilitar la lectura de los resultados, especialmente en sistemas con múltiples núcleos.