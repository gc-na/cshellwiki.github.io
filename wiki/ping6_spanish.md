# [Linux] Bash ping6 Uso: Comprobar la conectividad IPv6

## Overview
El comando `ping6` se utiliza para comprobar la conectividad de red en direcciones IPv6. Envía paquetes de eco ICMP a una dirección IP específica y espera respuestas, lo que permite verificar si un host está accesible a través de la red.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
ping6 [opciones] [argumentos]
```

## Common Options
- `-c <n>`: Especifica el número de paquetes de eco a enviar.
- `-i <segundos>`: Establece el intervalo entre envíos de paquetes.
- `-w <tiempo>`: Define el tiempo máximo de espera para recibir respuestas.
- `-s <tamaño>`: Establece el tamaño de los paquetes de eco enviados.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `ping6`:

1. **Comprobar la conectividad a un host específico:**
   ```bash
   ping6 google.com
   ```

2. **Enviar un número específico de paquetes:**
   ```bash
   ping6 -c 5 google.com
   ```

3. **Establecer un intervalo de envío de 2 segundos:**
   ```bash
   ping6 -i 2 google.com
   ```

4. **Enviar paquetes de un tamaño específico:**
   ```bash
   ping6 -s 128 google.com
   ```

5. **Limitar el tiempo de espera a 10 segundos:**
   ```bash
   ping6 -w 10 google.com
   ```

## Tips
- Utiliza la opción `-c` para evitar que el comando se ejecute indefinidamente, especialmente en pruebas de red.
- Asegúrate de que el host que estás probando tenga habilitado el soporte para IPv6.
- Puedes usar `ping6` junto con otras herramientas de red para diagnosticar problemas de conectividad más complejos.