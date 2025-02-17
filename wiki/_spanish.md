# [Linux] Bash @ uso: [ejecutar comandos en segundo plano]

## Overview
El comando `@` en Bash se utiliza para ejecutar comandos en segundo plano, permitiendo que el usuario continúe utilizando la terminal mientras se ejecutan otras tareas. Esto es especialmente útil para procesos que pueden tardar un tiempo considerable en completarse.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
@ [opciones] [argumentos]
```

## Common Options
- `&`: Coloca el comando en segundo plano.
- `disown`: Elimina el trabajo de la lista de trabajos, permitiendo que continúe ejecutándose incluso si se cierra la terminal.

## Common Examples
Aquí hay algunos ejemplos prácticos de cómo usar el comando `@`:

1. Ejecutar un script en segundo plano:
   ```bash
   ./mi_script.sh &
   ```

2. Ejecutar un comando largo y continuar usando la terminal:
   ```bash
   tar -czf archivo.tar.gz /ruta/al/directorio &
   ```

3. Desasociar un trabajo en segundo plano:
   ```bash
   sleep 60 &
   disown
   ```

4. Ejecutar múltiples comandos en segundo plano:
   ```bash
   comando1 & comando2 & comando3 &
   ```

## Tips
- Siempre verifica el estado de los trabajos en segundo plano usando el comando `jobs`.
- Utiliza `fg` para traer un trabajo en segundo plano de vuelta al primer plano si es necesario.
- Recuerda que los trabajos en segundo plano pueden generar salida en la terminal, así que redirige la salida si es necesario usando `> salida.txt` para evitar confusiones.