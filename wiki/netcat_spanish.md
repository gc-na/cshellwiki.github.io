# [Linux] Bash netcat uso: herramienta de red versátil

## Overview
El comando `netcat`, también conocido como "nc", es una herramienta de red que permite leer y escribir datos a través de conexiones de red utilizando el protocolo TCP o UDP. Es ampliamente utilizado para la depuración de redes y la transferencia de datos.

## Usage
La sintaxis básica del comando `netcat` es la siguiente:

```
netcat [opciones] [argumentos]
```

## Common Options
- `-l`: Escuchar en un puerto específico.
- `-p`: Especificar el puerto local.
- `-u`: Usar el protocolo UDP en lugar de TCP.
- `-v`: Modo verbose, muestra información adicional.
- `-z`: Escaneo de puertos, no envía datos.

## Common Examples
1. **Escuchar en un puerto específico**:
   ```bash
   netcat -l -p 1234
   ```

2. **Conectar a un servidor**:
   ```bash
   netcat example.com 80
   ```

3. **Transferir un archivo**:
   En el lado del servidor:
   ```bash
   netcat -l -p 1234 > archivo_recibido.txt
   ```
   En el lado del cliente:
   ```bash
   netcat servidor_ip 1234 < archivo_a_enviar.txt
   ```

4. **Escaneo de puertos**:
   ```bash
   netcat -z -v example.com 1-1000
   ```

## Tips
- Utiliza el modo verbose (`-v`) para obtener más información sobre lo que está haciendo `netcat`.
- Asegúrate de que el firewall no esté bloqueando los puertos que deseas usar.
- `netcat` puede ser una herramienta poderosa para pruebas de seguridad, pero úsala de manera ética y legal.