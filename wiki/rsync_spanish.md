# [Linux] Bash rsync Uso: Sincronizar archivos y directorios

## Overview
El comando `rsync` se utiliza para sincronizar archivos y directorios entre diferentes ubicaciones, ya sea en la misma máquina o entre máquinas remotas. Es eficiente porque solo copia los cambios realizados en los archivos, lo que ahorra tiempo y ancho de banda.

## Usage
La sintaxis básica del comando `rsync` es la siguiente:

```bash
rsync [opciones] [origen] [destino]
```

## Common Options
Aquí hay algunas opciones comunes que puedes usar con `rsync`:

- `-a`: Modo de archivo; copia archivos y directorios de manera recursiva y preserva atributos como permisos y tiempos de modificación.
- `-v`: Modo verbose; muestra información detallada sobre el proceso de sincronización.
- `-z`: Comprime los datos durante la transferencia, lo que puede acelerar la copia de archivos grandes.
- `-r`: Copia directorios de manera recursiva.
- `--delete`: Elimina archivos en el destino que no están presentes en el origen.

## Common Examples
Aquí tienes algunos ejemplos prácticos del uso de `rsync`:

1. **Sincronizar un directorio local:**
   ```bash
   rsync -av /ruta/al/origen/ /ruta/al/destino/
   ```

2. **Sincronizar a un servidor remoto:**
   ```bash
   rsync -av /ruta/al/origen/ usuario@servidor:/ruta/al/destino/
   ```

3. **Sincronizar desde un servidor remoto:**
   ```bash
   rsync -av usuario@servidor:/ruta/al/origen/ /ruta/al/destino/
   ```

4. **Sincronizar y eliminar archivos en el destino:**
   ```bash
   rsync -av --delete /ruta/al/origen/ /ruta/al/destino/
   ```

5. **Sincronizar con compresión:**
   ```bash
   rsync -avz /ruta/al/origen/ /ruta/al/destino/
   ```

## Tips
- Siempre es recomendable hacer una prueba con la opción `-n` (dry run) para ver qué archivos se copiarían sin realizar cambios reales.
- Utiliza la opción `-h` para mostrar los tamaños de archivo en un formato legible.
- Asegúrate de incluir la barra diagonal `/` al final de las rutas para evitar confusiones sobre si deseas copiar el contenido del directorio o el directorio en sí.