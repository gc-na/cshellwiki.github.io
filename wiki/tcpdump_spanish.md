# [Linux] Bash tcpdump Uso: Captura de paquetes de red

## Overview
El comando `tcpdump` es una herramienta de línea de comandos utilizada para capturar y analizar el tráfico de red que pasa a través de una interfaz de red en un sistema. Permite a los usuarios ver los paquetes que se envían y reciben, lo que es útil para la solución de problemas de red y el análisis de seguridad.

## Usage
La sintaxis básica del comando `tcpdump` es la siguiente:

```bash
tcpdump [opciones] [argumentos]
```

## Common Options
- `-i <interfaz>`: Especifica la interfaz de red a utilizar (por ejemplo, `eth0`).
- `-n`: No resuelve nombres de host, mostrando direcciones IP en su lugar.
- `-v`: Muestra información más detallada sobre los paquetes.
- `-c <número>`: Captura solo un número específico de paquetes.
- `-w <archivo>`: Guarda la salida de la captura en un archivo en lugar de mostrarla en la pantalla.
- `-r <archivo>`: Lee paquetes desde un archivo en lugar de una interfaz de red.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `tcpdump`:

1. Capturar paquetes en la interfaz `eth0`:
   ```bash
   tcpdump -i eth0
   ```

2. Capturar solo 10 paquetes y mostrar información detallada:
   ```bash
   tcpdump -i eth0 -c 10 -v
   ```

3. Guardar la captura de paquetes en un archivo llamado `captura.pcap`:
   ```bash
   tcpdump -i eth0 -w captura.pcap
   ```

4. Leer paquetes desde un archivo de captura:
   ```bash
   tcpdump -r captura.pcap
   ```

5. Capturar tráfico HTTP (puerto 80):
   ```bash
   tcpdump -i eth0 port 80
   ```

## Tips
- Asegúrate de tener permisos adecuados (puede requerir `sudo`) para capturar paquetes en la interfaz de red.
- Utiliza el flag `-n` para evitar la resolución de nombres y acelerar la captura.
- Filtra el tráfico por dirección IP o puerto para enfocarte en el tráfico relevante.
- Guarda las capturas en un archivo para un análisis posterior, especialmente si estás trabajando con un gran volumen de tráfico.