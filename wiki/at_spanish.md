# [Linux] Bash en at: Programar tareas para más tarde

## Overview
El comando `at` se utiliza en sistemas Unix y Linux para programar la ejecución de comandos o scripts en un momento específico en el futuro. Esto permite a los usuarios automatizar tareas sin necesidad de estar presentes en el momento de su ejecución.

## Usage
La sintaxis básica del comando `at` es la siguiente:

```bash
at [opciones] [hora]
```

## Common Options
- `-f archivo`: Especifica un archivo que contiene los comandos a ejecutar.
- `-m`: Envía un correo electrónico al usuario después de que se ejecute el comando, incluso si no se produce salida.
- `-q cola`: Permite especificar una cola de trabajo diferente para la tarea programada.
- `-V`: Muestra la versión del comando `at`.

## Common Examples
1. **Programar un comando para que se ejecute a una hora específica:**
   ```bash
   echo "echo 'Hola, mundo'" | at 14:00
   ```
   Este comando mostrará "Hola, mundo" a las 14:00.

2. **Programar un script para que se ejecute mañana a las 9 AM:**
   ```bash
   at 09:00 tomorrow -f /ruta/al/script.sh
   ```

3. **Programar un comando para que se ejecute en 5 minutos:**
   ```bash
   echo "backup.sh" | at now + 5 minutes
   ```

4. **Programar un comando y recibir un correo después de su ejecución:**
   ```bash
   echo "tar -czf backup.tar.gz /ruta/al/directorio" | at -m 02:00
   ```

## Tips
- Asegúrate de que el servicio `atd` esté en funcionamiento en tu sistema para que las tareas programadas se ejecuten correctamente.
- Puedes ver las tareas programadas con el comando `atq`.
- Para eliminar una tarea programada, utiliza `atrm [número de trabajo]`, donde el número de trabajo se obtiene con `atq`.