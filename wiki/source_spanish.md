# [Linux] Bash source uso equivalente: Ejecutar scripts en el contexto actual

## Overview
El comando `source` en Bash se utiliza para ejecutar un script en el contexto actual del shell. Esto significa que cualquier variable o función definida en el script estará disponible en la sesión actual después de que se ejecute el comando.

## Usage
La sintaxis básica del comando `source` es la siguiente:

```bash
source [opciones] [archivo]
```

También se puede usar el punto (`.`) como un alias para `source`:

```bash
. [archivo]
```

## Common Options
El comando `source` no tiene muchas opciones, pero aquí hay algunas que pueden ser útiles:

- `-e`: Permite que el script se ejecute en modo de depuración, mostrando cada comando antes de ejecutarlo.
- `-u`: Activa el modo estricto, que hace que el script falle si se intenta usar una variable no inicializada.

## Common Examples

### Ejecutar un script
Para ejecutar un script llamado `mi_script.sh` en el contexto actual, puedes usar:

```bash
source mi_script.sh
```
o
```bash
. mi_script.sh
```

### Cargar variables de entorno
Si tienes un archivo `variables.sh` que define algunas variables de entorno, puedes cargarlas así:

```bash
source variables.sh
```

### Usar en combinación con otros comandos
Puedes combinar `source` con otros comandos para ejecutar scripts que configuran el entorno antes de ejecutar un comando:

```bash
source setup_env.sh && ejecutar_comando
```

## Tips
- Siempre verifica que el script que estás cargando no contenga errores, ya que estos pueden afectar tu sesión actual.
- Usa `source` para cargar configuraciones personalizadas en tu archivo `.bashrc` o `.bash_profile` para que estén disponibles cada vez que inicies una nueva sesión de terminal.
- Recuerda que cualquier cambio en las variables de entorno realizado por el script persistirá en la sesión actual, así que ten cuidado al modificar variables importantes.