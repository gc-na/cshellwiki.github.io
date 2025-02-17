# [Linux] Bash iotop Uso: Monitorea el uso de I/O de los procesos

## Overview
El comando `iotop` es una herramienta de monitoreo en tiempo real que muestra el uso de entrada/salida (I/O) de los procesos en un sistema Linux. Es útil para identificar qué procesos están consumiendo más recursos de disco, lo que puede ayudar a diagnosticar problemas de rendimiento.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
iotop [opciones] [argumentos]
```

## Common Options
- `-o` o `--only`: Muestra solo los procesos que están realizando operaciones de I/O.
- `-b` o `--batch`: Ejecuta `iotop` en modo por lotes, útil para redirigir la salida a un archivo.
- `-d` o `--delay`: Establece el intervalo de actualización en segundos (por defecto es 1 segundo).
- `-p PID`: Muestra solo el proceso con el ID especificado.

## Common Examples
1. **Monitorear el uso de I/O en tiempo real:**
   ```bash
   iotop
   ```

2. **Mostrar solo procesos que están realizando operaciones de I/O:**
   ```bash
   iotop -o
   ```

3. **Ejecutar en modo por lotes y guardar la salida en un archivo:**
   ```bash
   iotop -b -n 10 > iotop_output.txt
   ```

4. **Establecer un intervalo de actualización de 2 segundos:**
   ```bash
   iotop -d 2
   ```

5. **Monitorear un proceso específico por su ID:**
   ```bash
   iotop -p 1234
   ```

## Tips
- Utiliza `iotop` con privilegios de superusuario (`sudo`) para obtener información completa sobre todos los procesos.
- Combina `iotop` con otras herramientas como `htop` para un monitoreo más completo del sistema.
- Si estás analizando un problema de rendimiento, observa los procesos que tienen un alto porcentaje de uso de I/O y considera investigar más sobre ellos.