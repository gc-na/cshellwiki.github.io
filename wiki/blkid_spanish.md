# [Linux] Bash blkid Uso: Identificar y mostrar información sobre dispositivos de bloques

## Overview
El comando `blkid` se utiliza en sistemas Linux para identificar y mostrar información sobre dispositivos de bloques, como particiones de disco y sistemas de archivos. Proporciona detalles como el tipo de sistema de archivos, el UUID y la etiqueta de cada dispositivo.

## Usage
La sintaxis básica del comando `blkid` es la siguiente:

```bash
blkid [opciones] [argumentos]
```

## Common Options
- `-o, --output`: Especifica el formato de salida (por ejemplo, `value`, `full`, `udev`).
- `-s, --match-tag`: Filtra la salida para mostrar solo las etiquetas especificadas.
- `-p, --probe`: Fuerza a `blkid` a buscar información en dispositivos que no están montados.
- `-c, --cache`: Utiliza un archivo de caché para mejorar el rendimiento.

## Common Examples
1. **Listar todos los dispositivos de bloques:**
   ```bash
   blkid
   ```

2. **Mostrar información en formato de valor:**
   ```bash
   blkid -o value
   ```

3. **Filtrar por una etiqueta específica:**
   ```bash
   blkid -s UUID
   ```

4. **Obtener información de un dispositivo específico:**
   ```bash
   blkid /dev/sda1
   ```

5. **Forzar la búsqueda en dispositivos no montados:**
   ```bash
   blkid -p
   ```

## Tips
- Utiliza `blkid` sin argumentos para obtener un resumen completo de todos los dispositivos de bloques disponibles.
- Si trabajas con sistemas de archivos, considera usar la opción `-o value` para obtener una salida más limpia y fácil de leer.
- Recuerda que algunos dispositivos pueden no estar montados, así que usa la opción `-p` si necesitas información sobre ellos.