# [Linux] Bash pidstat Uso: Monitoreo del rendimiento de procesos

## Overview
El comando `pidstat` se utiliza para monitorear el rendimiento de los procesos en un sistema Linux. Proporciona estadísticas sobre el uso de CPU, memoria y otros recursos para uno o más procesos en ejecución, lo que permite a los administradores del sistema identificar problemas de rendimiento.

## Usage
La sintaxis básica del comando `pidstat` es la siguiente:

```bash
pidstat [opciones] [argumentos]
```

## Common Options
- `-h`: Muestra la ayuda y la información sobre el uso del comando.
- `-p <pid>`: Especifica el ID del proceso que se desea monitorear.
- `-r`: Muestra estadísticas de uso de memoria.
- `-u`: Muestra estadísticas de uso de CPU.
- `-d`: Muestra estadísticas de uso de disco.
- `-t`: Muestra estadísticas para todos los hilos del proceso.

## Common Examples
1. **Monitorear todos los procesos:**
   ```bash
   pidstat
   ```

2. **Monitorear un proceso específico por su PID:**
   ```bash
   pidstat -p 1234
   ```

3. **Mostrar estadísticas de uso de CPU cada 2 segundos:**
   ```bash
   pidstat -u 2
   ```

4. **Mostrar estadísticas de uso de memoria para todos los procesos:**
   ```bash
   pidstat -r
   ```

5. **Monitorear todos los hilos de un proceso específico:**
   ```bash
   pidstat -p 1234 -t
   ```

## Tips
- Utiliza `pidstat` junto con otras herramientas como `top` o `htop` para obtener una visión más completa del rendimiento del sistema.
- Filtra los resultados para enfocarte en los procesos que realmente te interesan, utilizando el PID específico.
- Considera redirigir la salida a un archivo para un análisis posterior, usando `pidstat > salida.txt`.