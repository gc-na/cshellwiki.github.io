# [Linux] Bash tune2fs uso: Modificar parámetros de sistemas de archivos ext2/ext3/ext4

## Overview
El comando `tune2fs` se utiliza para ajustar los parámetros de los sistemas de archivos ext2, ext3 y ext4 en Linux. Permite modificar diversas configuraciones del sistema de archivos, como el tamaño de los bloques, las opciones de montaje y los límites de inodo, entre otros.

## Usage
La sintaxis básica del comando `tune2fs` es la siguiente:

```bash
tune2fs [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes que se pueden utilizar con `tune2fs`:

- `-c <número>`: Establece el número máximo de montajes antes de que se realice una verificación del sistema de archivos.
- `-i <intervalo>`: Establece el intervalo de tiempo entre las verificaciones del sistema de archivos.
- `-m <porcentaje>`: Establece el porcentaje de espacio reservado para el usuario root.
- `-O <opciones>`: Activa las características especificadas en el sistema de archivos.
- `-L <etiqueta>`: Cambia la etiqueta del sistema de archivos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `tune2fs`:

1. **Establecer el número máximo de montajes:**
   ```bash
   tune2fs -c 30 /dev/sda1
   ```

2. **Establecer un intervalo de verificación de 6 meses:**
   ```bash
   tune2fs -i 6m /dev/sda1
   ```

3. **Reservar el 5% del espacio para el usuario root:**
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. **Activar la característica de journaling:**
   ```bash
   tune2fs -O journal_data /dev/sda1
   ```

5. **Cambiar la etiqueta del sistema de archivos:**
   ```bash
   tune2fs -L "MiEtiqueta" /dev/sda1
   ```

## Tips
- Siempre realiza una copia de seguridad de tus datos antes de modificar los parámetros del sistema de archivos.
- Utiliza el comando `dumpe2fs` para obtener información detallada sobre el sistema de archivos antes de realizar cambios.
- Asegúrate de que el sistema de archivos esté desmontado o en modo de solo lectura antes de usar `tune2fs` para evitar daños.