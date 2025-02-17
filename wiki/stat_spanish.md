# [Linux] Bash stat Uso equivalente: Muestra información sobre archivos y sistemas de archivos

## Overview
El comando `stat` en Bash se utiliza para mostrar información detallada sobre archivos y sistemas de archivos. Proporciona datos como el tamaño del archivo, la fecha de creación, la última modificación y los permisos, entre otros.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
stat [opciones] [argumentos]
```

## Common Options
- `-c, --format=FORMATO`: Permite especificar un formato personalizado para la salida.
- `-f, --file-system`: Muestra información sobre el sistema de archivos en lugar de un archivo específico.
- `-L, --dereference`: Sigue los enlaces simbólicos y muestra la información del archivo al que apuntan.
- `--help`: Muestra la ayuda sobre el uso del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `stat`:

1. **Mostrar información básica de un archivo:**
   ```bash
   stat archivo.txt
   ```

2. **Mostrar información de un directorio:**
   ```bash
   stat /ruta/al/directorio
   ```

3. **Usar un formato personalizado para la salida:**
   ```bash
   stat -c '%n: %s bytes, Modificado: %y' archivo.txt
   ```

4. **Mostrar información del sistema de archivos:**
   ```bash
   stat -f /
   ```

5. **Seguir enlaces simbólicos:**
   ```bash
   stat -L enlace_simbolico
   ```

## Tips
- Utiliza el formato personalizado con `-c` para obtener solo la información que necesitas, lo que puede hacer que la salida sea más legible.
- Si trabajas con enlaces simbólicos, recuerda usar la opción `-L` para obtener información del archivo objetivo.
- Para obtener información rápida sobre el uso del comando, no dudes en usar `stat --help`.