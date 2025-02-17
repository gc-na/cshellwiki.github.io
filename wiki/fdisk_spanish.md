# [Linux] Bash fdisk Uso: Herramienta para gestionar particiones de disco

## Overview
El comando `fdisk` es una herramienta de línea de comandos utilizada para crear, eliminar y gestionar particiones en discos duros en sistemas Linux. Permite a los usuarios manipular la tabla de particiones de un dispositivo de almacenamiento.

## Usage
La sintaxis básica del comando `fdisk` es la siguiente:

```bash
fdisk [opciones] [dispositivo]
```

Donde `[dispositivo]` es el archivo de dispositivo que representa el disco que se desea gestionar, como `/dev/sda`.

## Common Options
- `-l`: Lista las particiones de todos los discos.
- `-u`: Muestra el tamaño de las particiones en sectores en lugar de cilindros.
- `-n`: Crea una nueva partición.
- `-d`: Elimina una partición existente.
- `-p`: Imprime la tabla de particiones del disco seleccionado.

## Common Examples
1. **Listar particiones de un disco:**
   ```bash
   fdisk -l /dev/sda
   ```

2. **Crear una nueva partición:**
   ```bash
   fdisk /dev/sda
   ```
   Luego, dentro de la interfaz de `fdisk`, puedes usar `n` para crear una nueva partición.

3. **Eliminar una partición:**
   ```bash
   fdisk /dev/sda
   ```
   Dentro de `fdisk`, usa `d` para eliminar una partición.

4. **Imprimir la tabla de particiones:**
   ```bash
   fdisk -p /dev/sda
   ```

## Tips
- Siempre realiza una copia de seguridad de tus datos antes de modificar particiones.
- Utiliza el comando `parted` si necesitas una interfaz más amigable para gestionar particiones.
- Asegúrate de desmontar cualquier partición antes de realizar cambios en ella para evitar la pérdida de datos.