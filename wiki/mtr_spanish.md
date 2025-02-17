# [Linux] Bash mtr Uso: Herramienta de diagnóstico de red

## Overview
El comando `mtr` (My Traceroute) combina las funcionalidades de `traceroute` y `ping` para proporcionar información sobre la ruta que toman los paquetes a través de una red. Es útil para diagnosticar problemas de conectividad y latencia en redes.

## Usage
La sintaxis básica del comando `mtr` es la siguiente:

```bash
mtr [opciones] [destino]
```

## Common Options
- `-r`: Ejecuta `mtr` en modo report, mostrando un resumen al final.
- `-c [n]`: Especifica el número de pings a enviar.
- `-i [segundos]`: Define el intervalo entre pings.
- `-p`: Muestra el puerto en el que se está realizando el ping.
- `-n`: No resuelve nombres de host, mostrando solo direcciones IP.

## Common Examples
1. **Ejecutar un mtr básico a un destino:**
   ```bash
   mtr google.com
   ```

2. **Ejecutar mtr en modo report con un número específico de pings:**
   ```bash
   mtr -r -c 10 google.com
   ```

3. **Ejecutar mtr sin resolver nombres de host:**
   ```bash
   mtr -n google.com
   ```

4. **Especificar un intervalo de 2 segundos entre pings:**
   ```bash
   mtr -i 2 google.com
   ```

5. **Mostrar el puerto utilizado:**
   ```bash
   mtr -p google.com
   ```

## Tips
- Utiliza el modo report (`-r`) para obtener un resumen claro de la conectividad.
- Ajusta el número de pings con `-c` para obtener resultados más precisos en conexiones inestables.
- Si estás depurando problemas de DNS, considera usar la opción `-n` para evitar la resolución de nombres que puede añadir latencia.