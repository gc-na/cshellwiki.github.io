# [Linux] Bash traceroute uso: Muestra la ruta que toman los paquetes en una red

## Overview
El comando `traceroute` se utiliza para rastrear la ruta que siguen los paquetes de datos desde un host hasta un destino específico en una red. Esto permite identificar los diferentes nodos o "saltos" que los paquetes atraviesan y puede ser útil para diagnosticar problemas de conectividad.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
traceroute [opciones] [destino]
```

## Common Options
- `-m <número>`: Establece el número máximo de saltos que se intentarán.
- `-p <puerto>`: Especifica el puerto que se utilizará para el envío de paquetes.
- `-w <segundos>`: Define el tiempo de espera para cada respuesta.
- `-I`: Utiliza paquetes ICMP en lugar de UDP.
- `-n`: Muestra las direcciones IP en lugar de intentar resolver los nombres de host.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `traceroute`:

1. **Rastrear la ruta a un dominio específico:**
   ```bash
   traceroute www.ejemplo.com
   ```

2. **Rastrear la ruta a una dirección IP:**
   ```bash
   traceroute 192.168.1.1
   ```

3. **Establecer un número máximo de saltos:**
   ```bash
   traceroute -m 10 www.ejemplo.com
   ```

4. **Utilizar paquetes ICMP:**
   ```bash
   traceroute -I www.ejemplo.com
   ```

5. **Mostrar direcciones IP sin resolver nombres:**
   ```bash
   traceroute -n www.ejemplo.com
   ```

## Tips
- Utiliza la opción `-n` si deseas obtener resultados más rápidos al evitar la resolución de nombres de host.
- Si estás experimentando problemas de red, observa los saltos donde se producen los retrasos o pérdidas de paquetes.
- Combina `traceroute` con otros comandos como `ping` para obtener un diagnóstico más completo de la conectividad de red.