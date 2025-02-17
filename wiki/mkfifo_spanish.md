# [Linux] Bash mkfifo Uso: Crear tuberías con nombre

El comando `mkfifo` se utiliza para crear tuberías con nombre en sistemas Unix y Linux, permitiendo la comunicación entre procesos.

## Overview
El comando `mkfifo` crea un archivo especial que actúa como una tubería con nombre. Esto permite que un proceso escriba datos en la tubería y otro proceso los lea, facilitando la comunicación interprocesos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
mkfifo [opciones] [nombre_del_fifo]
```

## Common Options
- `-m, --mode=MODE`: Establece los permisos del archivo FIFO. Por defecto, se utilizan los permisos del umask.
- `--help`: Muestra la ayuda sobre el comando.
- `--version`: Muestra la versión del comando.

## Common Examples

1. **Crear un FIFO simple:**
   ```bash
   mkfifo mi_fifo
   ```

2. **Crear un FIFO con permisos específicos:**
   ```bash
   mkfifo -m 666 mi_fifo
   ```

3. **Usar un FIFO en un comando de escritura:**
   ```bash
   echo "Hola, mundo" > mi_fifo
   ```

4. **Leer desde un FIFO en otro terminal:**
   ```bash
   cat mi_fifo
   ```

5. **Usar un FIFO en un script:**
   ```bash
   #!/bin/bash
   mkfifo mi_fifo
   echo "Mensaje desde el proceso 1" > mi_fifo &
   cat mi_fifo
   ```

## Tips
- Asegúrate de que el proceso que lee del FIFO esté en ejecución antes de escribir en él, ya que de lo contrario, el proceso de escritura se bloqueará.
- Utiliza permisos adecuados al crear el FIFO para evitar problemas de acceso.
- Recuerda que los FIFOs se eliminan automáticamente al cerrarse, pero puedes eliminarlos manualmente con `rm nombre_del_fifo`.