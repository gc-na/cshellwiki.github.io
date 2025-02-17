# [Linux] Bash command uso: [ejecutar comandos en segundo plano]

## Overview
El comando `nohup` permite ejecutar un comando en segundo plano, ignorando la señal de hangup (SIGHUP). Esto es útil para mantener procesos en ejecución incluso después de cerrar la sesión.

## Usage
La sintaxis básica del comando es la siguiente:

```
nohup comando [opciones] [argumentos] &
```

## Common Options
- `&`: Coloca el comando en segundo plano.
- `-p`: Permite especificar el proceso que se desea ejecutar en segundo plano.
- `-h`: Muestra la ayuda del comando.

## Common Examples
1. Ejecutar un script en segundo plano y redirigir la salida a un archivo:
   ```bash
   nohup ./mi_script.sh > salida.log &
   ```

2. Ejecutar un comando que tarda mucho tiempo en completarse:
   ```bash
   nohup long_running_command &
   ```

3. Ejecutar un comando y asegurarse de que no se detenga al cerrar la terminal:
   ```bash
   nohup python mi_programa.py &
   ```

## Tips
- Siempre redirige la salida a un archivo para evitar que se pierda información.
- Usa el comando `jobs` para ver los procesos en segundo plano.
- Puedes usar `fg` para traer un proceso en segundo plano de vuelta al primer plano si es necesario.