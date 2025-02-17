# [Linux] Bash lvextend Uso: Aumentar el tamaño de un volumen lógico

## Overview
El comando `lvextend` se utiliza en sistemas Linux para aumentar el tamaño de un volumen lógico en un grupo de volúmenes. Esto permite a los administradores de sistemas expandir el espacio de almacenamiento disponible sin necesidad de crear nuevos volúmenes.

## Usage
La sintaxis básica del comando `lvextend` es la siguiente:

```bash
lvextend [opciones] [argumentos]
```

## Common Options
- `-L +[tamaño]`: Aumenta el tamaño del volumen lógico en la cantidad especificada.
- `-l +[número]`: Aumenta el tamaño del volumen lógico en unidades de bloques lógicos.
- `-r`: Redimensiona el sistema de archivos automáticamente después de extender el volumen lógico.
- `-n [nombre]`: Cambia el nombre del volumen lógico.

## Common Examples
1. **Aumentar el tamaño de un volumen lógico en 10 GB:**
   ```bash
   lvextend -L +10G /dev/vg01/lv01
   ```

2. **Aumentar el tamaño de un volumen lógico utilizando bloques lógicos:**
   ```bash
   lvextend -l +100 /dev/vg01/lv01
   ```

3. **Aumentar el tamaño y redimensionar el sistema de archivos automáticamente:**
   ```bash
   lvextend -L +5G -r /dev/vg01/lv01
   ```

4. **Cambiar el nombre de un volumen lógico:**
   ```bash
   lvextend -n nuevo_nombre /dev/vg01/lv01
   ```

## Tips
- Siempre verifica el espacio disponible en el grupo de volúmenes antes de extender un volumen lógico utilizando el comando `vgs`.
- Realiza copias de seguridad de datos importantes antes de realizar cambios en los volúmenes lógicos.
- Utiliza la opción `-r` para redimensionar automáticamente el sistema de archivos, pero asegúrate de que el sistema de archivos sea compatible con esta operación.