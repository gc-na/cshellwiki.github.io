# [Linux] Bash top uso: Monitoreo de procesos en tiempo real

## Overview
El comando `top` es una herramienta de monitoreo en tiempo real que muestra los procesos en ejecución en un sistema Linux. Proporciona información sobre el uso de la CPU, la memoria y otros recursos del sistema, permitiendo a los usuarios identificar procesos que consumen muchos recursos.

## Usage
La sintaxis básica del comando `top` es la siguiente:

```bash
top [opciones] [argumentos]
```

## Common Options
- `-d <segundos>`: Establece el intervalo de actualización en segundos.
- `-n <número>`: Especifica el número de actualizaciones que se deben mostrar antes de salir.
- `-u <usuario>`: Muestra solo los procesos de un usuario específico.
- `-p <pid>`: Muestra solo el proceso con el ID de proceso especificado.

## Common Examples
1. **Ejecutar top con actualización cada 2 segundos:**
   ```bash
   top -d 2
   ```

2. **Mostrar solo los procesos de un usuario específico:**
   ```bash
   top -u nombre_usuario
   ```

3. **Limitar la salida a un número específico de actualizaciones:**
   ```bash
   top -n 5
   ```

4. **Monitorear un proceso específico por su PID:**
   ```bash
   top -p 1234
   ```

## Tips
- Para salir de la interfaz de `top`, presiona `q`.
- Puedes ordenar los procesos por diferentes columnas presionando las teclas correspondientes (por ejemplo, `M` para ordenar por uso de memoria).
- Usa la tecla `h` dentro de `top` para acceder a la ayuda y ver más opciones disponibles.