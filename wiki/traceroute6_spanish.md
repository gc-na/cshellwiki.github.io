# [Linux] Bash traceroute6 uso: Muestra la ruta de paquetes IPv6

## Overview
El comando `traceroute6` se utiliza para rastrear la ruta que siguen los paquetes IPv6 desde el host local hasta un destino específico. Proporciona información sobre cada salto en la red, lo que puede ser útil para diagnosticar problemas de conectividad.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
traceroute6 [opciones] [destino]
```

## Common Options
A continuación se presentan algunas opciones comunes para `traceroute6`:

- `-m <máximo_hops>`: Establece el número máximo de saltos que se intentarán.
- `-p <puerto>`: Especifica el puerto a utilizar para el envío de paquetes.
- `-w <tiempo>`: Define el tiempo de espera en segundos para cada respuesta.
- `-q <número>`: Establece el número de consultas por salto.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `traceroute6`:

1. Rastrear la ruta a un sitio web específico:
   ```bash
   traceroute6 www.ejemplo.com
   ```

2. Establecer un máximo de 15 saltos:
   ```bash
   traceroute6 -m 15 www.ejemplo.com
   ```

3. Usar un puerto específico (por ejemplo, el puerto 80):
   ```bash
   traceroute6 -p 80 www.ejemplo.com
   ```

4. Definir un tiempo de espera de 2 segundos:
   ```bash
   traceroute6 -w 2 www.ejemplo.com
   ```

5. Realizar 3 consultas por salto:
   ```bash
   traceroute6 -q 3 www.ejemplo.com
   ```

## Tips
- Asegúrate de tener privilegios adecuados para ejecutar `traceroute6`, ya que puede requerir permisos de superusuario en algunos sistemas.
- Utiliza la opción `-m` para limitar el número de saltos y evitar que el comando se ejecute indefinidamente en redes problemáticas.
- Si experimentas problemas de conectividad, compara los resultados de `traceroute6` con los de `ping` para obtener una visión más completa de la situación de la red.