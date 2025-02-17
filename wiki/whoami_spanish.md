# [Linux] Bash whoami Uso equivalente: Muestra el nombre del usuario actual

## Overview
El comando `whoami` en Bash se utiliza para mostrar el nombre de usuario del usuario que está actualmente conectado en la sesión de terminal. Es una herramienta sencilla pero útil para verificar la identidad del usuario en un entorno de línea de comandos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
whoami [opciones]
```

## Common Options
El comando `whoami` no tiene muchas opciones, pero aquí están las más comunes:

- `--help`: Muestra la ayuda sobre el uso del comando.
- `--version`: Muestra la versión del comando `whoami`.

## Common Examples

1. **Mostrar el nombre de usuario actual:**
   ```bash
   whoami
   ```

2. **Mostrar ayuda sobre el comando:**
   ```bash
   whoami --help
   ```

3. **Mostrar la versión del comando:**
   ```bash
   whoami --version
   ```

## Tips
- Utiliza `whoami` para confirmar que estás operando con el usuario correcto, especialmente antes de ejecutar comandos que requieren permisos elevados.
- Puedes combinar `whoami` con otros comandos en scripts para realizar acciones específicas basadas en el usuario actual.
- Recuerda que `whoami` es útil en entornos multiusuario para evitar confusiones sobre qué usuario está ejecutando un comando.