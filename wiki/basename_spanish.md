# [Linux] Bash basename Uso equivalente: Extraer el nombre de un archivo de una ruta

## Overview
El comando `basename` se utiliza en Bash para extraer el nombre de un archivo de una ruta completa. Esto es útil cuando deseas obtener solo el nombre del archivo sin la información del directorio.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
basename [opciones] [argumentos]
```

## Common Options
- `-a`: Permite procesar múltiples nombres de archivo.
- `-s`: Especifica un sufijo que se eliminará del nombre del archivo.
- `--help`: Muestra la ayuda del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `basename`:

1. **Extraer el nombre de un archivo de una ruta completa:**
   ```bash
   basename /ruta/al/archivo.txt
   ```
   Salida:
   ```
   archivo.txt
   ```

2. **Eliminar un sufijo específico:**
   ```bash
   basename /ruta/al/archivo.txt .txt
   ```
   Salida:
   ```
   archivo
   ```

3. **Procesar múltiples nombres de archivo:**
   ```bash
   basename -a /ruta/al/archivo1.txt /ruta/al/archivo2.txt
   ```
   Salida:
   ```
   archivo1.txt
   archivo2.txt
   ```

## Tips
- Utiliza `basename` en scripts para simplificar la manipulación de nombres de archivos.
- Combina `basename` con otros comandos como `find` para obtener resultados más específicos.
- Recuerda que `basename` solo devuelve el nombre del archivo; si necesitas la ruta, considera usar `dirname`.