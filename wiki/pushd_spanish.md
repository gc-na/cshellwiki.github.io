# [Linux] Bash pushd uso: Cambiar directorios de forma eficiente

## Overview
El comando `pushd` se utiliza en Bash para cambiar de directorio de manera eficiente, almacenando el directorio actual en una pila. Esto permite regresar fácilmente al directorio anterior utilizando el comando `popd`.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
pushd [opciones] [directorio]
```

## Common Options
- `+n`: Cambia al directorio en la posición `n` de la pila.
- `-n`: Cambia al directorio en la posición `n` de la pila, pero no lo elimina de la misma.
- `-`: Regresa al último directorio visitado.

## Common Examples
1. **Cambiar a un directorio específico y almacenar el actual:**
   ```bash
   pushd /ruta/al/directorio
   ```

2. **Regresar al directorio anterior:**
   ```bash
   popd
   ```

3. **Listar los directorios en la pila:**
   ```bash
   dirs
   ```

4. **Cambiar al segundo directorio en la pila:**
   ```bash
   pushd +1
   ```

5. **Regresar al último directorio y eliminarlo de la pila:**
   ```bash
   pushd -
   ```

## Tips
- Utiliza `dirs` para ver el estado actual de la pila de directorios.
- Combina `pushd` y `popd` para navegar rápidamente entre varios directorios sin perder la ubicación original.
- Recuerda que `pushd` puede ser útil en scripts para mantener un control sobre los directorios de trabajo.