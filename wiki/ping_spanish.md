# [Linux] Bash ping uso: Comprobar la conectividad de red

## Overview
El comando `ping` se utiliza para verificar la conectividad entre el host local y otro host en la red. Envía paquetes de datos ICMP Echo Request y espera recibir respuestas Echo Reply, lo que permite determinar si el destino es accesible y medir el tiempo de respuesta.

## Usage
La sintaxis básica del comando `ping` es la siguiente:

```bash
ping [opciones] [dirección]
```

## Common Options
- `-c [n]`: Envía un número específico de paquetes (n) y luego se detiene.
- `-i [segundos]`: Establece el intervalo de tiempo entre envíos de paquetes.
- `-t [ttl]`: Establece el valor TTL (Time To Live) de los paquetes enviados.
- `-s [tamaño]`: Especifica el tamaño de los paquetes de datos a enviar.

## Common Examples
1. **Ping a un host específico:**
   ```bash
   ping google.com
   ```

2. **Enviar solo 4 paquetes:**
   ```bash
   ping -c 4 google.com
   ```

3. **Ping con un intervalo de 2 segundos entre paquetes:**
   ```bash
   ping -i 2 google.com
   ```

4. **Especificar el tamaño del paquete:**
   ```bash
   ping -s 100 google.com
   ```

## Tips
- Utiliza `ping -c 4` para realizar pruebas rápidas sin saturar la red.
- Si no recibes respuestas, verifica la conexión a Internet o la dirección del host.
- Para un diagnóstico más detallado, combina `ping` con otras herramientas como `traceroute`.