# [Linux] Bash set uso: Configurar opciones de shell

## Overview
El comando `set` en Bash se utiliza para establecer o desactivar opciones del shell. Permite modificar el comportamiento del entorno de ejecución, lo que puede ser útil para depuración y control de flujo en scripts.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
set [opciones] [argumentos]
```

## Common Options
- `-e`: Hace que el script se detenga si un comando falla.
- `-u`: Trata las variables no definidas como un error y termina el script.
- `-x`: Muestra los comandos y sus argumentos a medida que se ejecutan, útil para depuración.
- `-o`: Permite establecer opciones específicas del shell, como `noclobber` o `pipefail`.

## Common Examples
1. **Detener el script en caso de error:**
   ```bash
   set -e
   ```
   Con esta opción, si un comando falla, el script se detendrá inmediatamente.

2. **Mostrar comandos en ejecución:**
   ```bash
   set -x
   ```
   Esto es útil para ver qué comandos se están ejecutando, lo que ayuda en la depuración.

3. **Evitar sobrescribir archivos:**
   ```bash
   set -o noclobber
   ```
   Esta opción impide que se sobrescriban archivos existentes al redirigir la salida.

4. **Tratar variables no definidas como error:**
   ```bash
   set -u
   ```
   Si intentas usar una variable que no ha sido definida, el script terminará con un error.

## Tips
- Utiliza `set -e` al inicio de tus scripts para evitar que continúen ejecutándose después de un error.
- Combina `set -x` con `set -e` para obtener un seguimiento detallado de los errores en tus scripts.
- Recuerda que algunas opciones pueden afectar el comportamiento de otros comandos, así que úsalas con precaución.