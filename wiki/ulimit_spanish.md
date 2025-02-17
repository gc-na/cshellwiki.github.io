# [Linux] Bash ulimit uso: Establecer límites de recursos del sistema

## Overview
El comando `ulimit` se utiliza en sistemas Unix y Linux para establecer límites en los recursos que pueden ser utilizados por los procesos en ejecución. Esto ayuda a prevenir que un solo proceso consuma todos los recursos del sistema, lo que podría afectar el rendimiento general.

## Usage
La sintaxis básica del comando `ulimit` es la siguiente:

```bash
ulimit [opciones] [argumentos]
```

## Common Options
- `-a`: Muestra todos los límites actuales.
- `-c`: Establece el tamaño máximo de los archivos de volcado de núcleo.
- `-d`: Establece el tamaño máximo de la memoria de datos.
- `-f`: Establece el tamaño máximo de los archivos que se pueden crear.
- `-l`: Establece el tamaño máximo de la memoria bloqueada.
- `-s`: Establece el tamaño máximo de la pila.
- `-t`: Establece el tiempo máximo de CPU en segundos.
- `-v`: Establece el tamaño máximo de la memoria virtual.

## Common Examples

1. **Mostrar todos los límites actuales:**

   ```bash
   ulimit -a
   ```

2. **Establecer el tamaño máximo de archivos a 100 MB:**

   ```bash
   ulimit -f 102400
   ```

3. **Limitar el tamaño de la pila a 8 MB:**

   ```bash
   ulimit -s 8192
   ```

4. **Establecer un límite de tiempo de CPU de 60 segundos:**

   ```bash
   ulimit -t 60
   ```

5. **Deshabilitar el volcado de núcleo:**

   ```bash
   ulimit -c 0
   ```

## Tips
- Siempre verifica los límites actuales con `ulimit -a` antes de realizar cambios.
- Los cambios realizados con `ulimit` son temporales y solo afectan a la sesión actual del shell.
- Para establecer límites permanentes, considera agregar configuraciones en archivos como `/etc/security/limits.conf`.
- Ten cuidado al aumentar los límites, ya que esto puede afectar la estabilidad del sistema si un proceso consume demasiados recursos.