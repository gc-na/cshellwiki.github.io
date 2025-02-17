# [Linux] Usuarios de Bash: Muestra información sobre los usuarios del sistema

## Overview
El comando `users` en Bash se utiliza para mostrar los nombres de los usuarios que han iniciado sesión en el sistema en un momento dado. Es una herramienta sencilla pero útil para obtener información rápida sobre la actividad de los usuarios en un sistema Linux.

## Usage
La sintaxis básica del comando `users` es la siguiente:

```bash
users [opciones] [argumentos]
```

## Common Options
- `-n`: Muestra el número de usuarios únicos que han iniciado sesión.
- `-r`: Muestra solo los usuarios que están actualmente conectados.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `users`:

1. **Mostrar usuarios conectados:**
   ```bash
   users
   ```

2. **Mostrar el número de usuarios únicos conectados:**
   ```bash
   users -n
   ```

3. **Mostrar solo usuarios conectados actualmente:**
   ```bash
   users -r
   ```

## Tips
- Utiliza el comando `who` para obtener información más detallada sobre los usuarios conectados, como la hora de inicio de sesión y el terminal utilizado.
- Combina `users` con otros comandos como `wc -l` para contar el número de usuarios conectados:
  ```bash
  users | wc -w
  ```
- Recuerda que `users` solo muestra los usuarios que están actualmente conectados, no proporciona información sobre los usuarios que han cerrado sesión.