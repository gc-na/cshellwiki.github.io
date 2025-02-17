# [Linux] Bash lvm uso: Gestión de volúmenes lógicos

## Overview
El comando `lvm` (Logical Volume Manager) se utiliza para gestionar volúmenes lógicos en sistemas Linux. Permite a los administradores de sistemas crear, eliminar y modificar volúmenes lógicos, facilitando la gestión del espacio en disco de manera flexible y eficiente.

## Usage
La sintaxis básica del comando `lvm` es la siguiente:

```bash
lvm [opciones] [argumentos]
```

## Common Options
- `create`: Crea un nuevo volumen lógico.
- `remove`: Elimina un volumen lógico existente.
- `extend`: Aumenta el tamaño de un volumen lógico.
- `reduce`: Disminuye el tamaño de un volumen lógico.
- `lvdisplay`: Muestra información sobre los volúmenes lógicos existentes.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `lvm`:

### Crear un volumen lógico
```bash
lvcreate -n mi_volumen -L 10G vg_mi_grupo
```

### Eliminar un volumen lógico
```bash
lvremove /dev/vg_mi_grupo/mi_volumen
```

### Ampliar un volumen lógico
```bash
lvextend -L +5G /dev/vg_mi_grupo/mi_volumen
```

### Reducir un volumen lógico
```bash
lvreduce -L -5G /dev/vg_mi_grupo/mi_volumen
```

### Mostrar información de volúmenes lógicos
```bash
lvdisplay
```

## Tips
- Siempre realiza copias de seguridad antes de modificar volúmenes lógicos, especialmente al reducir su tamaño.
- Utiliza `lvdisplay` para verificar el estado de los volúmenes lógicos antes y después de realizar cambios.
- Familiarízate con las opciones de `lvm` para aprovechar al máximo la gestión de volúmenes lógicos en tu sistema.