# [Linux] Bash parted Uso: Gestión de particiones de disco

## Overview
El comando `parted` se utiliza para gestionar particiones de disco en sistemas Linux. Permite crear, eliminar, redimensionar y modificar particiones de manera eficiente, facilitando la administración del espacio en disco.

## Usage
La sintaxis básica del comando `parted` es la siguiente:

```bash
parted [opciones] [argumentos]
```

## Common Options
- `-s`: Ejecuta `parted` en modo silencioso, sin mostrar mensajes de información.
- `mklabel`: Crea una nueva tabla de particiones en el disco.
- `mkpart`: Crea una nueva partición.
- `rm`: Elimina una partición existente.
- `resizepart`: Redimensiona una partición existente.
- `print`: Muestra la tabla de particiones actual.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `parted`:

### Crear una nueva tabla de particiones
```bash
parted /dev/sda mklabel gpt
```

### Crear una nueva partición
```bash
parted /dev/sda mkpart primary ext4 1MiB 100MiB
```

### Eliminar una partición
```bash
parted /dev/sda rm 1
```

### Redimensionar una partición
```bash
parted /dev/sda resizepart 1 200MiB
```

### Mostrar la tabla de particiones
```bash
parted /dev/sda print
```

## Tips
- Siempre realiza una copia de seguridad de tus datos antes de modificar particiones.
- Utiliza el modo interactivo de `parted` para una experiencia más guiada, simplemente ejecuta `parted /dev/sda` sin opciones adicionales.
- Verifica el sistema de archivos de las particiones antes de redimensionarlas para evitar la pérdida de datos.