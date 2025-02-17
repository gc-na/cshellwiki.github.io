# [Linux] Bash usermod uso: Modificar cuentas de usuario

## Overview
El comando `usermod` se utiliza en sistemas Linux para modificar las cuentas de usuario existentes. Permite cambiar atributos como el nombre de usuario, el grupo principal, los grupos secundarios y otros parámetros relacionados con la cuenta.

## Usage
La sintaxis básica del comando `usermod` es la siguiente:

```bash
usermod [opciones] [argumentos]
```

## Common Options
- `-l`: Cambia el nombre de usuario.
- `-d`: Cambia el directorio personal del usuario.
- `-m`: Mueve el contenido del directorio personal a la nueva ubicación.
- `-G`: Añade el usuario a uno o más grupos secundarios.
- `-s`: Cambia el intérprete de comandos (shell) del usuario.
- `-e`: Establece la fecha de expiración de la cuenta.

## Common Examples
1. **Cambiar el nombre de usuario:**
   ```bash
   usermod -l nuevo_usuario viejo_usuario
   ```

2. **Cambiar el directorio personal del usuario:**
   ```bash
   usermod -d /nuevo/directorio nuevo_usuario
   ```

3. **Mover el contenido del directorio personal:**
   ```bash
   usermod -d /nuevo/directorio -m nuevo_usuario
   ```

4. **Añadir un usuario a grupos secundarios:**
   ```bash
   usermod -G grupo1,grupo2 usuario
   ```

5. **Cambiar el intérprete de comandos del usuario:**
   ```bash
   usermod -s /bin/bash usuario
   ```

## Tips
- Siempre realiza una copia de seguridad de la información del usuario antes de hacer cambios significativos.
- Asegúrate de que el nuevo nombre de usuario o directorio no esté en uso por otro usuario.
- Utiliza el comando `id nombre_usuario` para verificar los grupos y el ID del usuario antes y después de realizar cambios.