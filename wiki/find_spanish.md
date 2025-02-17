# [Linux] Bash find uso: Buscar nombres de archivos

## Overview
El comando `find` en Bash se utiliza para buscar archivos y directorios en una jerarquía de directorios. Permite a los usuarios localizar archivos basándose en diferentes criterios como el nombre, el tipo, el tamaño, la fecha de modificación, entre otros.

## Usage
La sintaxis básica del comando `find` es la siguiente:

```bash
find [ruta] [opciones] [expresión]
```

## Common Options
- `-name`: Busca archivos que coincidan con un nombre específico.
- `-type`: Especifica el tipo de archivo a buscar (por ejemplo, `f` para archivos regulares, `d` para directorios).
- `-size`: Busca archivos que tengan un tamaño específico.
- `-mtime`: Busca archivos modificados en un período de tiempo específico.
- `-exec`: Permite ejecutar un comando en cada archivo encontrado.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `find`:

1. **Buscar un archivo por nombre:**
   ```bash
   find /ruta/al/directorio -name "archivo.txt"
   ```

2. **Buscar todos los directorios:**
   ```bash
   find /ruta/al/directorio -type d
   ```

3. **Buscar archivos de un tamaño específico (por ejemplo, mayores de 1MB):**
   ```bash
   find /ruta/al/directorio -size +1M
   ```

4. **Buscar archivos modificados en los últimos 7 días:**
   ```bash
   find /ruta/al/directorio -mtime -7
   ```

5. **Ejecutar un comando en cada archivo encontrado (por ejemplo, eliminar archivos .tmp):**
   ```bash
   find /ruta/al/directorio -name "*.tmp" -exec rm {} \;
   ```

## Tips
- Utiliza comillas alrededor de los nombres de archivo que contienen caracteres especiales o espacios.
- Combina opciones para hacer búsquedas más específicas, como buscar archivos de un tipo y tamaño particular.
- Siempre verifica el resultado de tu búsqueda antes de ejecutar comandos destructivos, como `-exec rm`, para evitar la eliminación accidental de archivos importantes.