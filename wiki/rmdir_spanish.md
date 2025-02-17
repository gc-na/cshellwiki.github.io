# [Linux] Bash rmdir Uso: Eliminar directorios vacíos

## Overview
El comando `rmdir` se utiliza en Bash para eliminar directorios que están vacíos. Si intentas eliminar un directorio que contiene archivos o subdirectorios, el comando fallará y no realizará ninguna acción.

## Usage
La sintaxis básica del comando `rmdir` es la siguiente:

```
rmdir [opciones] [argumentos]
```

## Common Options
- `-p`: Elimina el directorio especificado y sus directorios padre si están vacíos.
- `--ignore-fail-on-non-empty`: No muestra un error si el directorio no está vacío.
- `--verbose`: Muestra un mensaje por cada directorio que se elimina.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `rmdir`:

1. **Eliminar un directorio vacío:**
   ```bash
   rmdir mi_directorio
   ```

2. **Eliminar un directorio vacío y sus padres:**
   ```bash
   rmdir -p padre/hijo
   ```

3. **Eliminar un directorio vacío y mostrar un mensaje:**
   ```bash
   rmdir --verbose mi_directorio
   ```

4. **Ignorar errores si el directorio no está vacío:**
   ```bash
   rmdir --ignore-fail-on-non-empty mi_directorio
   ```

## Tips
- Asegúrate de que el directorio esté vacío antes de usar `rmdir`, ya que de lo contrario, el comando no funcionará.
- Utiliza la opción `-p` para eliminar directorios de forma recursiva, pero solo si estás seguro de que los directorios padre también están vacíos.
- Considera usar `rmdir` en scripts de limpieza para mantener tu sistema organizado, eliminando directorios que ya no se necesitan.