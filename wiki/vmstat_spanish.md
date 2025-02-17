# [Linux] Bash vmstat Uso: Monitoreo del rendimiento del sistema

## Overview
El comando `vmstat` (Virtual Memory Statistics) se utiliza para mostrar información sobre la memoria virtual, procesos, entradas/salidas y el estado del sistema. Es una herramienta útil para el monitoreo del rendimiento del sistema en tiempo real.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
vmstat [opciones] [intervalo] [número]
```

## Common Options
- `-a`: Muestra estadísticas de memoria activa y inactiva.
- `-m`: Muestra estadísticas de la memoria de páginas.
- `-s`: Muestra un resumen de las estadísticas de memoria.
- `-d`: Muestra estadísticas de disco.
- `intervalo`: Especifica el intervalo de tiempo en segundos entre las actualizaciones de la salida.
- `número`: Especifica cuántas veces se debe mostrar la salida.

## Common Examples
1. **Mostrar estadísticas de memoria cada 2 segundos:**
   ```bash
   vmstat 2
   ```

2. **Mostrar estadísticas de memoria activa e inactiva:**
   ```bash
   vmstat -a
   ```

3. **Mostrar un resumen de las estadísticas de memoria:**
   ```bash
   vmstat -s
   ```

4. **Mostrar estadísticas de disco cada 5 segundos, 10 veces:**
   ```bash
   vmstat -d 5 10
   ```

## Tips
- Utiliza `vmstat` junto con otros comandos como `top` o `iostat` para obtener una visión más completa del rendimiento del sistema.
- Monitorea el uso de memoria y procesos durante períodos de alta carga para identificar cuellos de botella.
- Considera redirigir la salida a un archivo para análisis posterior, utilizando `vmstat 2 > salida.txt`.