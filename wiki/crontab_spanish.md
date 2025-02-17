# [Linux] Bash crontab Uso: Programar tareas automáticamente

## Overview
El comando `crontab` se utiliza para programar tareas que se ejecutan automáticamente en intervalos regulares en sistemas Unix y Linux. Permite a los usuarios definir comandos o scripts que se ejecutarán en momentos específicos, facilitando la automatización de tareas repetitivas.

## Usage
La sintaxis básica del comando `crontab` es la siguiente:

```
crontab [opciones] [archivo]
```

## Common Options
- `-e`: Editar el archivo crontab del usuario actual.
- `-l`: Listar las tareas programadas en el crontab del usuario actual.
- `-r`: Eliminar el archivo crontab del usuario actual.
- `-i`: Solicitar confirmación antes de eliminar el crontab.

## Common Examples
Aquí hay algunos ejemplos prácticos de cómo usar `crontab`:

1. **Editar el crontab**:
   Para editar el crontab del usuario actual, utiliza:
   ```bash
   crontab -e
   ```

2. **Listar tareas programadas**:
   Para ver las tareas programadas, ejecuta:
   ```bash
   crontab -l
   ```

3. **Eliminar el crontab**:
   Para eliminar todas las tareas programadas, usa:
   ```bash
   crontab -r
   ```

4. **Programar una tarea para que se ejecute cada día a las 2 AM**:
   Para ejecutar un script llamado `backup.sh` todos los días a las 2 AM, añade la siguiente línea al crontab:
   ```bash
   0 2 * * * /ruta/al/script/backup.sh
   ```

5. **Programar una tarea cada hora**:
   Para ejecutar un comando cada hora, puedes usar:
   ```bash
   0 * * * * /ruta/al/comando
   ```

## Tips
- Asegúrate de usar rutas absolutas para los scripts y comandos en el crontab para evitar problemas de localización.
- Revisa los logs del sistema para verificar si tus tareas programadas se están ejecutando correctamente.
- Utiliza comentarios en tu crontab (precedidos por `#`) para documentar qué hace cada tarea, lo que facilitará su mantenimiento.