# [Linux] Bash ftp uso: Interactuar con servidores FTP

## Overview
El comando `ftp` se utiliza para transferir archivos entre un cliente y un servidor utilizando el protocolo File Transfer Protocol (FTP). Permite a los usuarios conectarse a servidores FTP, subir y bajar archivos, y gestionar directorios en el servidor.

## Usage
La sintaxis básica del comando `ftp` es la siguiente:

```bash
ftp [opciones] [argumentos]
```

## Common Options
- `-i`: Desactiva el modo interactivo, lo que permite la transferencia de archivos sin solicitar confirmación.
- `-n`: Evita que `ftp` intente iniciar sesión automáticamente.
- `-v`: Muestra información detallada sobre la conexión y la transferencia de archivos.
- `-p`: Utiliza un puerto pasivo para la conexión, lo que puede ser útil en redes con firewalls.

## Common Examples

### Conectar a un servidor FTP
```bash
ftp ftp.ejemplo.com
```

### Subir un archivo al servidor
```bash
put archivo.txt
```

### Descargar un archivo del servidor
```bash
get archivo.txt
```

### Cambiar de directorio en el servidor
```bash
cd /ruta/del/directorio
```

### Listar archivos en el directorio actual del servidor
```bash
ls
```

### Salir de la sesión FTP
```bash
bye
```

## Tips
- Asegúrate de tener las credenciales correctas para conectarte al servidor FTP.
- Utiliza el modo pasivo (`-p`) si tienes problemas de conexión en redes restringidas.
- Recuerda que la transferencia de archivos a través de FTP no es segura; considera usar SFTP o FTPS para mayor seguridad.