# [Linux] Bash watch uso: Monitorear la salida de un comando

## Overview
El comando `watch` en Bash se utiliza para ejecutar un comando de forma periódica y mostrar su salida en la terminal. Esto es útil para monitorear cambios en la salida de un comando sin necesidad de ejecutarlo manualmente cada vez.

## Usage
La sintaxis básica del comando `watch` es la siguiente:

```bash
watch [options] [arguments]
```

## Common Options
- `-n, --interval`: Especifica el intervalo de tiempo en segundos entre cada ejecución del comando. Por defecto, es 2 segundos.
- `-d, --differences`: Resalta las diferencias entre la salida de las ejecuciones sucesivas.
- `-t, --no-title`: Suprime la línea de título que muestra la hora y el comando que se está ejecutando.
- `-x, --exec`: Permite ejecutar un comando que no es un shell.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `watch`:

1. Monitorear el uso de la memoria:
   ```bash
   watch -n 5 free -h
   ```

2. Ver los procesos en ejecución y su uso de CPU:
   ```bash
   watch -d ps aux --sort=-%cpu
   ```

3. Supervisar los cambios en un archivo de registro:
   ```bash
   watch tail -n 10 /var/log/syslog
   ```

4. Comprobar la conectividad de red a un host específico:
   ```bash
   watch -n 2 ping -c 1 google.com
   ```

## Tips
- Utiliza la opción `-d` para resaltar los cambios, lo que facilita la identificación de diferencias en la salida.
- Ajusta el intervalo con `-n` según tus necesidades; un intervalo más corto puede ser útil para cambios rápidos, mientras que uno más largo puede ser suficiente para cambios más lentos.
- Si deseas ejecutar un comando que requiere privilegios de superusuario, puedes usar `sudo` junto con `watch`.