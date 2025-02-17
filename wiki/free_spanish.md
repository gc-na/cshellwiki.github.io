# [Linux] Bash free uso: Muestra el uso de memoria del sistema

## Overview
El comando `free` se utiliza en sistemas Linux para mostrar información sobre la memoria del sistema, incluyendo la memoria total, utilizada, libre y la memoria de intercambio (swap). Es una herramienta útil para monitorear el rendimiento del sistema y la disponibilidad de recursos.

## Usage
La sintaxis básica del comando `free` es la siguiente:

```bash
free [opciones]
```

## Common Options
- `-h`: Muestra la memoria en un formato legible por humanos (ej. MB, GB).
- `-m`: Muestra la memoria en megabytes.
- `-g`: Muestra la memoria en gigabytes.
- `-s [segundos]`: Actualiza la información cada cierto número de segundos.
- `-t`: Muestra un total de la memoria utilizada y libre.

## Common Examples
1. **Mostrar información básica de memoria:**
   ```bash
   free
   ```

2. **Mostrar información en un formato legible por humanos:**
   ```bash
   free -h
   ```

3. **Mostrar la memoria en megabytes:**
   ```bash
   free -m
   ```

4. **Actualizar la información cada 5 segundos:**
   ```bash
   free -s 5
   ```

5. **Mostrar el total de memoria utilizada y libre:**
   ```bash
   free -t
   ```

## Tips
- Utiliza la opción `-h` para facilitar la lectura de los resultados, especialmente en sistemas con mucha memoria.
- Combina `free` con otros comandos como `watch` para monitorear el uso de memoria en tiempo real:
  ```bash
  watch free -h
  ```
- Revisa la memoria de intercambio (swap) para asegurarte de que el sistema no esté utilizando demasiada memoria virtual, lo que puede afectar el rendimiento.