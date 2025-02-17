# [Linux] Bash wait Uso equivalente: Esperar la finalización de procesos

El comando `wait` se utiliza en Bash para esperar a que finalicen uno o más procesos en segundo plano.

## Overview
El comando `wait` permite que un script o terminal se detenga hasta que un proceso específico o todos los procesos en segundo plano hayan terminado. Esto es útil para sincronizar la ejecución de comandos y asegurarse de que ciertos procesos se completen antes de continuar con otros.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
wait [opciones] [argumentos]
```

## Common Options
- `-n`: Espera a que finalice cualquier proceso en segundo plano.
- `PID`: Especifica el ID del proceso (PID) para el que se desea esperar.

## Common Examples

1. **Esperar a que un proceso específico termine:**
   ```bash
   sleep 5 &  # Inicia un proceso en segundo plano
   wait $!    # Espera a que el proceso en segundo plano termine
   ```

2. **Esperar a que todos los procesos en segundo plano terminen:**
   ```bash
   sleep 3 &  # Inicia un proceso en segundo plano
   sleep 4 &  # Inicia otro proceso en segundo plano
   wait       # Espera a que todos los procesos en segundo plano terminen
   ```

3. **Usar wait con un PID específico:**
   ```bash
   sleep 2 &  # Inicia un proceso en segundo plano
   pid=$!     # Captura el PID del proceso
   wait $pid  # Espera a que el proceso con el PID específico termine
   ```

4. **Esperar a cualquier proceso en segundo plano:**
   ```bash
   sleep 1 &  # Inicia un proceso en segundo plano
   sleep 2 &  # Inicia otro proceso en segundo plano
   wait -n    # Espera a que cualquiera de los procesos en segundo plano termine
   ```

## Tips
- Utiliza `wait` para garantizar que los procesos en segundo plano se completen antes de continuar con el siguiente paso en tu script.
- Siempre captura el PID de un proceso en segundo plano si planeas usar `wait` para ese proceso específico.
- Recuerda que `wait` no solo se utiliza para procesos que iniciaste, sino también para cualquier proceso en segundo plano que se esté ejecutando en la misma sesión de terminal.