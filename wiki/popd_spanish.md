# [Linux] Bash popd Uso equivalente: Regresar al directorio anterior

El comando `popd` se utiliza para cambiar al directorio que se encuentra en la parte superior de la pila de directorios, eliminando ese directorio de la pila.

## Overview
El comando `popd` es parte de la gestión de directorios en Bash, que permite a los usuarios navegar entre directorios de manera eficiente. Funciona en conjunto con el comando `pushd`, que agrega directorios a la pila. Al usar `popd`, puedes volver rápidamente al último directorio visitado sin tener que escribir la ruta completa.

## Usage
La sintaxis básica del comando `popd` es la siguiente:

```bash
popd [options] [arguments]
```

## Common Options
- `+n`: Regresa al directorio en la posición `n` de la pila.
- `-n`: Regresa al directorio en la posición `n` desde el final de la pila.

## Common Examples
1. **Regresar al último directorio**:
   ```bash
   popd
   ```

2. **Regresar al segundo directorio en la pila**:
   ```bash
   popd +1
   ```

3. **Regresar al directorio en la segunda posición desde el final**:
   ```bash
   popd -2
   ```

4. **Usar popd después de pushd**:
   ```bash
   pushd /ruta/al/directorio1
   pushd /ruta/al/directorio2
   popd  # Regresa a /ruta/al/directorio1
   ```

## Tips
- Asegúrate de usar `pushd` antes de `popd` para que la pila de directorios tenga elementos.
- Puedes verificar el contenido de la pila de directorios usando el comando `dirs`.
- Utiliza `popd +n` para navegar a directorios específicos en la pila sin tener que recordar las rutas.