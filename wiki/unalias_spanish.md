# [Linux] Bash unalias uso: Eliminar alias de comandos

## Overview
El comando `unalias` se utiliza en Bash para eliminar alias previamente definidos. Los alias son atajos que permiten ejecutar comandos más largos o complejos con una palabra o frase más corta. Al usar `unalias`, puedes deshacerte de estos atajos cuando ya no los necesites.

## Usage
La sintaxis básica del comando `unalias` es la siguiente:

```
unalias [opciones] [argumentos]
```

## Common Options
- `-a`: Elimina todos los alias definidos en la sesión actual.
- `-p`: Muestra todos los alias actuales sin eliminarlos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `unalias`:

1. **Eliminar un alias específico**:
   Si tienes un alias llamado `ll` que se refiere a `ls -l`, puedes eliminarlo con el siguiente comando:
   ```bash
   unalias ll
   ```

2. **Eliminar todos los alias**:
   Para eliminar todos los alias definidos en la sesión actual, utiliza la opción `-a`:
   ```bash
   unalias -a
   ```

3. **Mostrar todos los alias actuales**:
   Para ver todos los alias que has definido sin eliminarlos, puedes usar la opción `-p`:
   ```bash
   unalias -p
   ```

## Tips
- Asegúrate de que realmente deseas eliminar un alias antes de usar `unalias`, ya que no hay una opción de deshacer.
- Puedes agregar el comando `unalias` en tu archivo de configuración de shell (como `.bashrc`) si deseas eliminar un alias cada vez que inicies una nueva sesión.
- Recuerda que los alias son específicos de la sesión actual a menos que se definan en un archivo de configuración, así que verifica si el alias se volverá a crear en futuras sesiones.