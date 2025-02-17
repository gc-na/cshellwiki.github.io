# [Linux] Bash chage Uso: Cambiar la información de caducidad de contraseñas

## Overview
El comando `chage` se utiliza en sistemas Linux para modificar la información relacionada con la caducidad de las contraseñas de los usuarios. Permite establecer políticas de caducidad y notificación, ayudando a mejorar la seguridad del sistema.

## Usage
La sintaxis básica del comando `chage` es la siguiente:

```bash
chage [opciones] [argumentos]
```

## Common Options
- `-l`: Muestra la información de caducidad de la contraseña para un usuario específico.
- `-m`: Establece el número mínimo de días entre cambios de contraseña.
- `-M`: Establece el número máximo de días que una contraseña es válida.
- `-I`: Establece el número de días de inactividad antes de que la cuenta sea desactivada.
- `-E`: Establece la fecha de expiración de la cuenta.

## Common Examples
1. **Mostrar información de caducidad de la contraseña de un usuario:**
   ```bash
   chage -l nombre_usuario
   ```

2. **Establecer un mínimo de 7 días entre cambios de contraseña:**
   ```bash
   chage -m 7 nombre_usuario
   ```

3. **Establecer un máximo de 30 días de validez para la contraseña:**
   ```bash
   chage -M 30 nombre_usuario
   ```

4. **Configurar 15 días de inactividad antes de desactivar la cuenta:**
   ```bash
   chage -I 15 nombre_usuario
   ```

5. **Establecer la fecha de expiración de la cuenta para el 1 de enero de 2024:**
   ```bash
   chage -E 2024-01-01 nombre_usuario
   ```

## Tips
- Siempre verifica la configuración de caducidad después de realizar cambios utilizando `chage -l nombre_usuario`.
- Considera establecer recordatorios para los usuarios sobre la caducidad de sus contraseñas.
- Utiliza `chage` junto con otras herramientas de administración de usuarios para mantener una buena política de seguridad.