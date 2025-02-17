# [Linux] Bash dig Uso equivalente: consulta de DNS

## Overview
El comando `dig` (Domain Information Groper) se utiliza para realizar consultas DNS (Domain Name System). Permite a los usuarios obtener información sobre registros DNS, lo que es útil para la resolución de nombres de dominio y la depuración de problemas de red.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
dig [opciones] [argumentos]
```

## Common Options
- `@server`: Especifica un servidor DNS diferente para realizar la consulta.
- `-t tipo`: Define el tipo de registro DNS a consultar (por ejemplo, A, AAAA, MX).
- `+short`: Muestra una salida más corta, mostrando solo la información relevante.
- `-x dirección`: Realiza una búsqueda inversa para obtener el nombre de dominio asociado a una dirección IP.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `dig`:

1. **Consulta de un registro A:**
   ```bash
   dig example.com
   ```

2. **Consulta de un registro MX:**
   ```bash
   dig -t MX example.com
   ```

3. **Consulta a un servidor DNS específico:**
   ```bash
   dig @8.8.8.8 example.com
   ```

4. **Búsqueda inversa de una dirección IP:**
   ```bash
   dig -x 8.8.8.8
   ```

5. **Salida corta de un registro A:**
   ```bash
   dig +short example.com
   ```

## Tips
- Utiliza la opción `+trace` para seguir la cadena de servidores DNS hasta llegar a la respuesta final.
- Para obtener información detallada sobre la consulta, puedes usar la opción `+stats`.
- Recuerda que algunas consultas pueden ser almacenadas en caché, por lo que es útil usar `+nocache` para evitar resultados en caché.