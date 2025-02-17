# [Linux] Bash write uso equivalente: Enviar mensajes a otros usuarios

## Overview
El comando `write` en Bash se utiliza para enviar mensajes de texto a otros usuarios que están conectados al mismo sistema. Es una herramienta útil para la comunicación rápida entre usuarios en entornos multiusuario.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
write [usuario] [tty]
```

Donde `[usuario]` es el nombre del usuario al que deseas enviar el mensaje y `[tty]` es el terminal específico (opcional).

## Common Options
- `-n`: No espera a que el usuario esté listo para recibir el mensaje.
- `-h`: No muestra el mensaje de "escribiendo" al destinatario.

## Common Examples
1. Enviar un mensaje a un usuario específico:
   ```bash
   write juan
   ```
   Luego de ejecutar este comando, puedes escribir tu mensaje y presionar `Ctrl+D` para enviarlo.

2. Enviar un mensaje a un usuario en un terminal específico:
   ```bash
   write juan pts/1
   ```
   Esto enviará el mensaje a Juan que está conectado en el terminal `pts/1`.

3. Usar la opción `-n` para enviar un mensaje sin esperar:
   ```bash
   write -n juan
   ```
   Esto permite enviar el mensaje inmediatamente sin esperar a que Juan esté listo.

## Tips
- Asegúrate de que el usuario al que deseas enviar el mensaje esté conectado y tenga permisos para recibir mensajes.
- Puedes usar `who` para ver qué usuarios están conectados y en qué terminales.
- Recuerda que el destinatario puede silenciar los mensajes usando el comando `mesg n`, así que verifica si está disponible para recibir tus mensajes.