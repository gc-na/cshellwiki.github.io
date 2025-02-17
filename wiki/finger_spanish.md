# [Linux] Bash finger uso: Muestra información sobre usuarios del sistema

## Overview
El comando `finger` se utiliza para mostrar información sobre los usuarios que están registrados en el sistema. Proporciona detalles como el nombre completo, la hora de inicio de sesión, el tiempo de inactividad y la ubicación del usuario, entre otros.

## Usage
La sintaxis básica del comando `finger` es la siguiente:

```bash
finger [opciones] [argumentos]
```

## Common Options
- `-l`: Muestra la información en un formato más detallado.
- `-m`: Ignora las mayúsculas en los nombres de usuario.
- `-s`: Muestra un resumen breve de la información del usuario.
- `-p`: No muestra la información de la dirección de correo electrónico.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `finger`:

1. Mostrar información de todos los usuarios:
   ```bash
   finger
   ```

2. Mostrar información detallada de un usuario específico:
   ```bash
   finger nombre_usuario
   ```

3. Mostrar un resumen breve de todos los usuarios:
   ```bash
   finger -s
   ```

4. Mostrar información de un usuario sin la dirección de correo electrónico:
   ```bash
   finger -p nombre_usuario
   ```

5. Ignorar mayúsculas al buscar un usuario:
   ```bash
   finger -m NOMBRE_USUARIO
   ```

## Tips
- Utiliza `finger` en combinación con otros comandos como `grep` para filtrar la información que necesitas.
- Recuerda que la información mostrada por `finger` depende de la configuración del sistema y de los permisos de los usuarios.
- Es útil para administradores de sistemas que necesitan supervisar el estado de los usuarios en el sistema.