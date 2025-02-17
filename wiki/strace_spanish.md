# [Linux] Bash strace Uso: Herramienta para rastrear llamadas al sistema

## Overview
El comando `strace` es una herramienta poderosa en Linux que permite rastrear las llamadas al sistema y las señales que recibe un proceso. Es útil para depurar programas y entender cómo interactúan con el sistema operativo.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
strace [options] [arguments]
```

## Common Options
- `-c`: Resumen de estadísticas de las llamadas al sistema.
- `-e trace=<set>`: Especifica qué llamadas al sistema rastrear.
- `-p <pid>`: Adjunta `strace` a un proceso existente utilizando su ID de proceso.
- `-o <file>`: Redirige la salida a un archivo en lugar de la consola.
- `-f`: Sigue los procesos hijos creados por el proceso rastreado.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `strace`:

1. **Rastrear un comando simple:**
   ```bash
   strace ls
   ```

2. **Rastrear un proceso en ejecución:**
   ```bash
   strace -p 1234
   ```
   (Reemplace `1234` con el ID del proceso que desea rastrear).

3. **Guardar la salida en un archivo:**
   ```bash
   strace -o salida.txt ls
   ```

4. **Rastrear solo las llamadas de apertura de archivos:**
   ```bash
   strace -e trace=open ls
   ```

5. **Obtener un resumen de estadísticas:**
   ```bash
   strace -c ls
   ```

## Tips
- Utiliza `strace` con `-f` para rastrear procesos hijos, especialmente útil en aplicaciones que crean múltiples subprocesos.
- Redirigir la salida a un archivo puede facilitar el análisis posterior, especialmente para procesos que generan mucha información.
- Familiarízate con las diferentes categorías de llamadas al sistema para filtrar la información relevante durante el rastreo.