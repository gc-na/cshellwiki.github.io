# [Linux] Bash nslookup uso: Consulta de direcciones DNS

## Overview
El comando `nslookup` se utiliza para consultar el sistema de nombres de dominio (DNS) para obtener información sobre direcciones IP y nombres de dominio. Permite a los usuarios resolver nombres de dominio a direcciones IP y viceversa, lo que es fundamental para la navegación en Internet y la administración de redes.

## Usage
La sintaxis básica del comando `nslookup` es la siguiente:

```bash
nslookup [opciones] [argumentos]
```

## Common Options
- `-type=tipo`: Especifica el tipo de registro DNS que se desea consultar (por ejemplo, A, AAAA, MX, etc.).
- `-timeout=segundos`: Establece el tiempo de espera para recibir una respuesta.
- `-retry=número`: Define el número de intentos de consulta en caso de fallo.
- `-debug`: Muestra información de depuración adicional sobre la consulta.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `nslookup`:

1. **Consultar la dirección IP de un dominio:**
   ```bash
   nslookup www.ejemplo.com
   ```

2. **Consultar un registro MX (Mail Exchange) de un dominio:**
   ```bash
   nslookup -type=MX ejemplo.com
   ```

3. **Consultar la dirección IP de un dominio específico utilizando un servidor DNS diferente:**
   ```bash
   nslookup www.ejemplo.com 8.8.8.8
   ```

4. **Obtener información de depuración sobre una consulta:**
   ```bash
   nslookup -debug www.ejemplo.com
   ```

## Tips
- Siempre verifica que estás utilizando el servidor DNS correcto, especialmente si estás realizando pruebas de conectividad.
- Usa el tipo de registro adecuado para obtener la información específica que necesitas.
- Considera utilizar la opción `-timeout` si estás en una red lenta para evitar esperas prolongadas.