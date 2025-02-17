# [Linux] Bash exit uso: Finaliza un script o una sesión de terminal

## Overview
El comando `exit` en Bash se utiliza para finalizar un script o cerrar una sesión de terminal. Este comando permite salir de un script de manera controlada y, opcionalmente, devolver un código de estado que puede ser utilizado por otros procesos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
exit [número]
```

Donde `[número]` es un código de salida opcional que indica el estado de la finalización. Por defecto, si no se proporciona un número, se utiliza el código de salida del último comando ejecutado.

## Common Options
- `número`: Un entero que representa el código de salida. Por convención, un código de salida de `0` indica éxito, mientras que cualquier otro número indica un error o un estado específico.

## Common Examples

1. **Salir de un script sin especificar un código de salida:**
   ```bash
   #!/bin/bash
   echo "Este script se está cerrando."
   exit
   ```

2. **Salir de un script con un código de salida específico:**
   ```bash
   #!/bin/bash
   echo "Ocurrió un error."
   exit 1
   ```

3. **Salir de la terminal actual:**
   ```bash
   exit
   ```

4. **Salir de la terminal y devolver un código de salida:**
   ```bash
   exit 0
   ```

## Tips
- Siempre es buena práctica especificar un código de salida en scripts para facilitar la depuración y el manejo de errores.
- Utiliza `exit 0` para indicar que un script se completó con éxito y `exit 1` o cualquier otro número para indicar un error.
- Recuerda que al salir de un script, todos los procesos en segundo plano iniciados por el script también se cerrarán.