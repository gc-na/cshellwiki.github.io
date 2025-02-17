# [Linux] Bash lsblk Uso: Muestra información sobre dispositivos de bloques

## Overview
El comando `lsblk` se utiliza para listar información sobre todos los dispositivos de bloques disponibles en el sistema, como discos duros, particiones y dispositivos de almacenamiento extraíbles. Este comando es útil para obtener una visión general de la estructura de almacenamiento en un sistema Linux.

## Usage
La sintaxis básica del comando `lsblk` es la siguiente:

```bash
lsblk [opciones] [argumentos]
```

## Common Options
- `-a`, `--all`: Muestra todos los dispositivos, incluidos los que no tienen un sistema de archivos.
- `-f`, `--fs`: Muestra información sobre los sistemas de archivos en los dispositivos.
- `-l`, `--list`: Muestra la salida en formato de lista en lugar de árbol.
- `-o`, `--output`: Especifica las columnas que se deben mostrar en la salida.
- `-p`, `--paths`: Muestra las rutas completas de los dispositivos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `lsblk`:

1. **Listar todos los dispositivos de bloques:**
   ```bash
   lsblk
   ```

2. **Listar todos los dispositivos, incluidos los que no tienen sistema de archivos:**
   ```bash
   lsblk -a
   ```

3. **Mostrar información sobre los sistemas de archivos:**
   ```bash
   lsblk -f
   ```

4. **Mostrar la salida en formato de lista:**
   ```bash
   lsblk -l
   ```

5. **Especificar columnas para mostrar:**
   ```bash
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tips
- Utiliza `lsblk -f` para obtener información detallada sobre los sistemas de archivos, lo que puede ser útil al gestionar particiones.
- Combina `lsblk` con otros comandos como `grep` para filtrar la salida y encontrar dispositivos específicos.
- Recuerda que `lsblk` no requiere privilegios de superusuario, lo que lo hace accesible para todos los usuarios en el sistema.