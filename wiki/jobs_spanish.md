# [Linux] Bash jobs uso: Gestionar trabajos en segundo plano

## Overview
El comando `jobs` en Bash se utiliza para mostrar la lista de trabajos que se están ejecutando en segundo plano en la sesión actual del terminal. Esto incluye trabajos que se han suspendido o que están en ejecución. Es una herramienta útil para gestionar y supervisar procesos que no están en primer plano.

## Usage
La sintaxis básica del comando `jobs` es la siguiente:

```bash
jobs [opciones]
```

## Common Options
- `-l`: Muestra el número de proceso (PID) junto con la información del trabajo.
- `-n`: Muestra solo los trabajos que han cambiado de estado desde la última vez que se ejecutó el comando.
- `-p`: Muestra solo los identificadores de proceso de los trabajos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `jobs`:

1. **Mostrar trabajos en segundo plano:**
   ```bash
   jobs
   ```

2. **Mostrar trabajos con PID:**
   ```bash
   jobs -l
   ```

3. **Mostrar trabajos que han cambiado de estado:**
   ```bash
   jobs -n
   ```

4. **Mostrar solo los identificadores de proceso:**
   ```bash
   jobs -p
   ```

## Tips
- Utiliza `bg` para reanudar un trabajo suspendido en segundo plano después de haberlo detenido con `Ctrl + Z`.
- Usa `fg` para llevar un trabajo en segundo plano de vuelta al primer plano.
- Recuerda que los trabajos en segundo plano seguirán ejecutándose incluso si cierras la terminal, a menos que se detengan explícitamente.