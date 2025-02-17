# [Linux] Bash mount uso: Montar sistemas de archivos

## Overview
El comando `mount` en Bash se utiliza para montar sistemas de archivos en el sistema operativo Linux. Esto permite que el sistema acceda a los datos almacenados en dispositivos de almacenamiento, como discos duros, unidades USB o particiones.

## Usage
La sintaxis básica del comando `mount` es la siguiente:

```bash
mount [opciones] [dispositivo] [punto_de_montaje]
```

## Common Options
- `-t tipo`: Especifica el tipo de sistema de archivos (por ejemplo, ext4, ntfs).
- `-o opciones`: Permite especificar opciones adicionales para el montaje (como `ro` para solo lectura).
- `-a`: Monta todos los sistemas de archivos mencionados en el archivo `/etc/fstab`.
- `-r`: Monta el sistema de archivos en modo solo lectura.

## Common Examples
1. Montar un dispositivo USB en un punto de montaje específico:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Montar un sistema de archivos NTFS en modo lectura y escritura:
   ```bash
   mount -t ntfs-3g -o rw /dev/sdc1 /mnt/ntfs
   ```

3. Montar todos los sistemas de archivos definidos en `/etc/fstab`:
   ```bash
   mount -a
   ```

4. Montar un sistema de archivos en modo solo lectura:
   ```bash
   mount -o ro /dev/sda1 /mnt/data
   ```

## Tips
- Asegúrate de que el punto de montaje exista antes de intentar montar un dispositivo.
- Utiliza el comando `umount` para desmontar un sistema de archivos de manera segura.
- Verifica los sistemas de archivos montados con el comando `df -h` para asegurarte de que se han montado correctamente.