# [Linux] Bash resize2fs Uso: Redimensionar sistemas de archivos ext2/ext3/ext4

## Overview
El comando `resize2fs` se utiliza para redimensionar sistemas de archivos ext2, ext3 y ext4. Permite aumentar o disminuir el tamaño del sistema de archivos de acuerdo con el tamaño de la partición en la que reside.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
resize2fs [opciones] [argumentos]
```

## Common Options
- `-f`: Forzar el redimensionamiento incluso si el sistema de archivos está montado.
- `-p`: Mostrar el progreso durante el redimensionamiento.
- `-s`: Redimensionar el sistema de archivos a un tamaño específico.
- `-M`: Reducir el sistema de archivos al tamaño mínimo posible.

## Common Examples
1. **Aumentar el tamaño del sistema de archivos al tamaño máximo de la partición**:
   ```bash
   resize2fs /dev/sda1
   ```

2. **Redimensionar el sistema de archivos a un tamaño específico (por ejemplo, 20G)**:
   ```bash
   resize2fs /dev/sda1 20G
   ```

3. **Forzar el redimensionamiento de un sistema de archivos montado**:
   ```bash
   resize2fs -f /dev/sda1
   ```

4. **Mostrar el progreso durante el redimensionamiento**:
   ```bash
   resize2fs -p /dev/sda1
   ```

## Tips
- Siempre realiza una copia de seguridad de tus datos antes de redimensionar un sistema de archivos.
- Asegúrate de que el sistema de archivos esté desmontado si planeas reducir su tamaño.
- Verifica el estado del sistema de archivos con `e2fsck` antes de usar `resize2fs` para evitar problemas.