# [Linux] Bash lvcreate Uso: Crear volúmenes lógicos en LVM

## Overview
El comando `lvcreate` se utiliza en Linux para crear volúmenes lógicos dentro de un grupo de volúmenes en el sistema de gestión de volúmenes lógicos (LVM). Esto permite la gestión eficiente del almacenamiento, facilitando la creación, eliminación y redimensionamiento de volúmenes.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
lvcreate [opciones] [argumentos]
```

## Common Options
- `-n, --name <nombre>`: Especifica el nombre del volumen lógico que se va a crear.
- `-L, --size <tamaño>`: Define el tamaño del volumen lógico a crear.
- `-l, --extents <número>`: Especifica el número de extensiones a utilizar para el volumen lógico.
- `-C, --mirrored`: Crea un volumen lógico espejo.
- `-Z, --zero n`: Controla si se debe inicializar el volumen lógico con ceros.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `lvcreate`:

1. **Crear un volumen lógico de 10 GB:**
   ```bash
   lvcreate -L 10G -n mi_volumen vg01
   ```

2. **Crear un volumen lógico de 5 extensiones:**
   ```bash
   lvcreate -l 5 -n volumen_extendido vg01
   ```

3. **Crear un volumen lógico espejo:**
   ```bash
   lvcreate -m 1 -n volumen_espejo -L 20G vg01
   ```

4. **Crear un volumen lógico y formatearlo con ext4:**
   ```bash
   lvcreate -L 15G -n volumen_formateado vg01
   mkfs.ext4 /dev/vg01/volumen_formateado
   ```

## Tips
- Asegúrate de tener suficiente espacio libre en el grupo de volúmenes antes de crear un nuevo volumen lógico.
- Utiliza nombres descriptivos para los volúmenes lógicos para facilitar su identificación en el futuro.
- Considera el uso de volúmenes lógicos espejo para mejorar la redundancia y la disponibilidad de los datos.