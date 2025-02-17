# [Linux] Bash logout uso: Cerrar sesión en la terminal

## Overview
El comando `logout` se utiliza en entornos de terminal para cerrar la sesión del usuario actual. Es especialmente útil en sesiones de shell de login, donde se desea salir de manera ordenada y liberar recursos del sistema.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
logout [options]
```

## Common Options
El comando `logout` no tiene muchas opciones, pero aquí hay algunas que pueden ser útiles:

- `-f`: Forzar el cierre de sesión sin preguntar.
- `-n`: No ejecutar el script de cierre de sesión.

## Common Examples

### Ejemplo 1: Cerrar sesión normalmente
Para cerrar la sesión de la terminal actual, simplemente escribe:

```bash
logout
```

### Ejemplo 2: Forzar el cierre de sesión
Si deseas cerrar la sesión sin confirmación, puedes usar la opción `-f`:

```bash
logout -f
```

### Ejemplo 3: Cerrar sesión en un script
Si estás ejecutando un script y deseas cerrar la sesión al final, puedes incluir el comando `logout` al final del script:

```bash
#!/bin/bash
# Tu script aquí
logout
```

## Tips
- Asegúrate de guardar tu trabajo antes de ejecutar `logout`, ya que cerrará la sesión y perderás cualquier trabajo no guardado.
- Utiliza `exit` en lugar de `logout` si estás en un subshell o en una sesión no de login.
- Si estás utilizando un entorno gráfico, considera cerrar la sesión a través de la interfaz en lugar de usar el comando `logout`.