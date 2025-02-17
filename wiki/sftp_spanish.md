# [Linux] Bash sftp uso: Transferir archivos de manera segura

## Overview
El comando `sftp` (Secure File Transfer Protocol) se utiliza para transferir archivos de manera segura entre un cliente y un servidor a través de una conexión SSH. Proporciona una interfaz interactiva similar a FTP, pero con la seguridad adicional que ofrece SSH.

## Usage
La sintaxis básica del comando `sftp` es la siguiente:

```bash
sftp [opciones] [usuario@host]
```

## Common Options
- `-P [puerto]`: Especifica el puerto a utilizar para la conexión.
- `-i [archivo]`: Utiliza la clave privada especificada para la autenticación.
- `-b [archivo]`: Ejecuta comandos de SFTP desde un archivo en lugar de la entrada estándar.
- `-v`: Muestra información detallada sobre la conexión y las operaciones.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `sftp`:

1. Conectar a un servidor SFTP:
   ```bash
   sftp usuario@servidor.com
   ```

2. Transferir un archivo desde el cliente al servidor:
   ```bash
   put archivo.txt
   ```

3. Descargar un archivo del servidor al cliente:
   ```bash
   get archivo.txt
   ```

4. Cambiar el directorio en el servidor:
   ```bash
   cd /ruta/del/directorio
   ```

5. Listar archivos en el directorio actual del servidor:
   ```bash
   ls
   ```

## Tips
- Siempre verifica la conexión utilizando el comando `ls` para asegurarte de que estás en el directorio correcto antes de transferir archivos.
- Usa la opción `-v` para depurar problemas de conexión si encuentras errores.
- Considera usar claves SSH para una autenticación más segura en lugar de contraseñas.