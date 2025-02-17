# [Linux] Bash netstat Uso: Muestra conexiones de red y estadísticas

## Overview
El comando `netstat` es una herramienta de red que permite visualizar las conexiones de red activas, las tablas de enrutamiento, las interfaces de red y las estadísticas de protocolo. Es útil para diagnosticar problemas de red y monitorizar el estado de las conexiones.

## Usage
La sintaxis básica del comando `netstat` es la siguiente:

```bash
netstat [opciones] [argumentos]
```

## Common Options
- `-a`: Muestra todas las conexiones y puertos de escucha.
- `-t`: Muestra solo las conexiones TCP.
- `-u`: Muestra solo las conexiones UDP.
- `-n`: Muestra las direcciones y números de puerto en formato numérico.
- `-l`: Muestra solo los puertos que están en estado de escucha.
- `-p`: Muestra el identificador del proceso (PID) y el nombre del programa que está utilizando la conexión.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `netstat`:

1. **Mostrar todas las conexiones y puertos de escucha:**
   ```bash
   netstat -a
   ```

2. **Mostrar solo conexiones TCP:**
   ```bash
   netstat -t
   ```

3. **Mostrar conexiones UDP:**
   ```bash
   netstat -u
   ```

4. **Mostrar conexiones en formato numérico:**
   ```bash
   netstat -n
   ```

5. **Mostrar puertos en estado de escucha:**
   ```bash
   netstat -l
   ```

6. **Mostrar conexiones junto con el PID del proceso:**
   ```bash
   netstat -p
   ```

## Tips
- Combina opciones para obtener información más específica. Por ejemplo, `netstat -tuln` muestra todas las conexiones TCP y UDP en estado de escucha en formato numérico.
- Usa `netstat` junto con otros comandos como `grep` para filtrar resultados. Por ejemplo:
  ```bash
  netstat -tuln | grep 80
  ```
- Recuerda que en algunos sistemas, puede que necesites permisos de superusuario para ver información detallada sobre los procesos.