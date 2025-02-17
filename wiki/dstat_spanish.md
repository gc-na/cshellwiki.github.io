# [Linux] Bash dstat Uso: Monitoreo de recursos del sistema en tiempo real

## Overview
El comando `dstat` es una herramienta versátil que permite monitorear y visualizar el rendimiento del sistema en tiempo real. Combina las funcionalidades de varios comandos como `vmstat`, `iostat`, `netstat`, y otros, proporcionando una vista integral de los recursos del sistema, incluyendo CPU, memoria, disco y red.

## Usage
La sintaxis básica del comando `dstat` es la siguiente:

```bash
dstat [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes que se pueden utilizar con `dstat`:

- `-c`: Muestra el uso de la CPU.
- `-d`: Muestra la actividad del disco.
- `-n`: Muestra la actividad de la red.
- `-m`: Muestra el uso de la memoria.
- `-t`: Muestra la marca de tiempo en la salida.
- `--full`: Muestra todas las estadísticas disponibles.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `dstat`:

1. **Monitorear el uso de la CPU y la memoria:**

   ```bash
   dstat -c -m
   ```

2. **Ver la actividad del disco y de la red:**

   ```bash
   dstat -d -n
   ```

3. **Monitorear todos los recursos con marcas de tiempo:**

   ```bash
   dstat -t --full
   ```

4. **Guardar la salida en un archivo para análisis posterior:**

   ```bash
   dstat -t -c -d -n --output salida.csv
   ```

## Tips
- Utiliza `dstat` con diferentes combinaciones de opciones para obtener una visión más completa del rendimiento del sistema.
- Considera redirigir la salida a un archivo si planeas analizar los datos más tarde.
- Familiarízate con las opciones de `dstat` para personalizar la visualización según tus necesidades específicas.