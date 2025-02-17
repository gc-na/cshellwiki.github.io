# [Linux] Bash hash uso: Gestiona el caché de comandos

## Overview
El comando `hash` en Bash se utiliza para gestionar el caché de comandos. Este comando permite almacenar la ubicación de los comandos ejecutados, lo que puede acelerar la búsqueda de estos en futuras ejecuciones.

## Usage
La sintaxis básica del comando `hash` es la siguiente:

```bash
hash [opciones] [argumentos]
```

## Common Options
- `-r`: Borra el caché de comandos, forzando a Bash a volver a buscar la ubicación de los comandos.
- `-p`: Especifica una ruta para un comando en particular, actualizando su ubicación en el caché.
- `-l`: Muestra el contenido actual del caché de comandos.

## Common Examples

1. **Mostrar el caché de comandos actual:**
   ```bash
   hash
   ```

2. **Borrar el caché de comandos:**
   ```bash
   hash -r
   ```

3. **Actualizar la ubicación de un comando específico:**
   ```bash
   hash -p /usr/local/bin/nuevo_comando nuevo_comando
   ```

4. **Listar el caché de comandos con sus rutas:**
   ```bash
   hash -l
   ```

## Tips
- Utiliza `hash -r` después de instalar nuevos programas para asegurarte de que Bash reconozca las nuevas ubicaciones de los comandos.
- Revisa el caché de comandos regularmente con `hash` para optimizar el rendimiento de tus sesiones de terminal.
- Si cambias la ubicación de un comando, considera usar `hash -p` para actualizar su ruta en el caché y evitar errores de "comando no encontrado".