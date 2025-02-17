# [Linux] Bash id uso: Muestra información sobre el usuario actual

## Overview
El comando `id` en Bash se utiliza para mostrar información sobre el usuario actual, incluyendo su identificador de usuario (UID), identificador de grupo (GID) y los grupos a los que pertenece. Es una herramienta útil para verificar los permisos y la configuración del usuario en el sistema.

## Usage
La sintaxis básica del comando `id` es la siguiente:

```bash
id [opciones] [argumentos]
```

## Common Options
- `-u`: Muestra solo el UID del usuario.
- `-g`: Muestra solo el GID del grupo principal del usuario.
- `-G`: Muestra todos los GIDs de los grupos a los que pertenece el usuario.
- `-n`: Muestra los nombres en lugar de los números de UID y GID.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `id`:

1. **Mostrar información del usuario actual**:
   ```bash
   id
   ```

2. **Mostrar solo el UID del usuario actual**:
   ```bash
   id -u
   ```

3. **Mostrar solo el GID del grupo principal del usuario actual**:
   ```bash
   id -g
   ```

4. **Mostrar todos los GIDs de los grupos a los que pertenece el usuario actual**:
   ```bash
   id -G
   ```

5. **Mostrar el nombre del usuario y su UID**:
   ```bash
   id -un
   ```

## Tips
- Utiliza `id` sin opciones para obtener un resumen completo de la información del usuario.
- Recuerda que puedes combinar opciones, por ejemplo, `id -u -n` para obtener el nombre del usuario junto con su UID.
- Es útil para scripts de Bash donde necesitas verificar los permisos del usuario antes de ejecutar ciertas acciones.