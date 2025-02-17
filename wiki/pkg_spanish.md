# [Linux] Bash pkg uso: Gestión de paquetes en sistemas Linux

## Overview
El comando `pkg` se utiliza para gestionar paquetes en sistemas operativos basados en Unix, especialmente en FreeBSD. Permite a los usuarios instalar, actualizar y eliminar software de manera eficiente.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
pkg [opciones] [argumentos]
```

## Common Options
- `install`: Instala uno o más paquetes.
- `remove`: Elimina uno o más paquetes.
- `update`: Actualiza la lista de paquetes disponibles.
- `upgrade`: Actualiza todos los paquetes instalados a sus versiones más recientes.
- `search`: Busca un paquete específico en los repositorios.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `pkg`:

1. **Instalar un paquete**:
   ```bash
   pkg install nombre_del_paquete
   ```

2. **Eliminar un paquete**:
   ```bash
   pkg remove nombre_del_paquete
   ```

3. **Actualizar la lista de paquetes**:
   ```bash
   pkg update
   ```

4. **Actualizar todos los paquetes instalados**:
   ```bash
   pkg upgrade
   ```

5. **Buscar un paquete**:
   ```bash
   pkg search nombre_del_paquete
   ```

## Tips
- Siempre ejecuta `pkg update` antes de instalar o actualizar paquetes para asegurarte de que tienes la lista más reciente.
- Utiliza `pkg info nombre_del_paquete` para obtener información detallada sobre un paquete específico.
- Considera usar `pkg autoremove` para eliminar paquetes que ya no son necesarios y liberar espacio en disco.