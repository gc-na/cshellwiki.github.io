# [Linux] Bash du uso: Muestra el uso del disco de archivos y directorios

## Overview
El comando `du` (disk usage) se utiliza en sistemas Unix y Linux para estimar y mostrar el uso del espacio en disco de archivos y directorios. Permite a los usuarios identificar qué archivos o carpetas están ocupando más espacio en el sistema.

## Usage
La sintaxis básica del comando `du` es la siguiente:

```bash
du [opciones] [argumentos]
```

## Common Options
- `-h`: Muestra el tamaño en un formato legible por humanos (por ejemplo, KB, MB, GB).
- `-s`: Muestra solo el total para cada argumento, sin listar los subdirectorios.
- `-a`: Incluye archivos en la salida, no solo directorios.
- `-c`: Muestra un total acumulado al final de la salida.
- `--max-depth=N`: Limita la profundidad de los directorios que se muestran a N niveles.

## Common Examples
1. **Mostrar el uso del disco de un directorio específico:**
   ```bash
   du /ruta/al/directorio
   ```

2. **Mostrar el uso del disco en un formato legible por humanos:**
   ```bash
   du -h /ruta/al/directorio
   ```

3. **Mostrar solo el total del uso del disco para un directorio:**
   ```bash
   du -sh /ruta/al/directorio
   ```

4. **Incluir archivos en la salida:**
   ```bash
   du -ah /ruta/al/directorio
   ```

5. **Limitar la profundidad de los directorios mostrados:**
   ```bash
   du --max-depth=1 -h /ruta/al/directorio
   ```

6. **Mostrar un total acumulado:**
   ```bash
   du -ch /ruta/al/directorio
   ```

## Tips
- Utiliza la opción `-h` para facilitar la lectura de los tamaños, especialmente en directorios grandes.
- Combina `-s` con `-h` para obtener un resumen claro del uso del disco de varios directorios.
- Si estás buscando archivos que ocupan mucho espacio, considera usar `du -ah` y luego canalizar la salida a `sort` para ordenar los resultados.