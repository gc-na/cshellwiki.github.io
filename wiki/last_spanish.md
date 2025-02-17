# [Linux] Bash last uso: Muestra los últimos inicios de sesión

## Overview
El comando `last` se utiliza en sistemas Unix y Linux para mostrar una lista de los últimos inicios de sesión de los usuarios. Esta información se extrae del archivo de registro `/var/log/wtmp`, que mantiene un historial de todos los inicios y cierres de sesión.

## Usage
La sintaxis básica del comando `last` es la siguiente:

```bash
last [opciones] [argumentos]
```

## Common Options
- `-a`: Muestra la dirección IP o el nombre de host del usuario que se ha conectado.
- `-n [número]`: Limita la salida a los últimos `número` de inicios de sesión.
- `-R`: Suprime la impresión del nombre del host.
- `-x`: Muestra información sobre los inicios de sesión y los apagados del sistema.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `last`:

1. **Mostrar todos los inicios de sesión:**
   ```bash
   last
   ```

2. **Mostrar los últimos 5 inicios de sesión:**
   ```bash
   last -n 5
   ```

3. **Mostrar inicios de sesión con direcciones IP:**
   ```bash
   last -a
   ```

4. **Mostrar información de apagados del sistema:**
   ```bash
   last -x
   ```

5. **Filtrar por un usuario específico:**
   ```bash
   last nombre_usuario
   ```

## Tips
- Utiliza `last -n 10` para revisar rápidamente los últimos 10 inicios de sesión.
- Puedes combinar opciones, como `last -a -n 5`, para obtener una salida más específica.
- Revisa el archivo `/var/log/wtmp` si necesitas más información sobre los registros de inicio de sesión.