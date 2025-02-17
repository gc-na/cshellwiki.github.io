# [Linux] Bash who uso equivalente: Muestra quién está conectado al sistema

## Overview
El comando `who` se utiliza en sistemas Unix y Linux para mostrar una lista de los usuarios que están actualmente conectados al sistema. Proporciona información sobre el nombre de usuario, la terminal, la fecha y hora de inicio de sesión, así como la dirección IP o el nombre del host desde donde se conectaron.

## Usage
La sintaxis básica del comando `who` es la siguiente:

```
who [opciones] [argumentos]
```

## Common Options
- `-a`: Muestra toda la información disponible, incluyendo usuarios, tiempos de inactividad y más.
- `-b`: Muestra la última vez que se reinició el sistema.
- `-q`: Muestra solo los nombres de los usuarios conectados y el número total de usuarios.
- `--help`: Muestra la ayuda del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `who`:

1. **Mostrar todos los usuarios conectados:**
   ```bash
   who
   ```

2. **Mostrar información detallada de los usuarios conectados:**
   ```bash
   who -a
   ```

3. **Mostrar la última vez que se reinició el sistema:**
   ```bash
   who -b
   ```

4. **Mostrar solo los nombres de los usuarios conectados:**
   ```bash
   who -q
   ```

5. **Mostrar información de un usuario específico:**
   ```bash
   who username
   ```

## Tips
- Utiliza `who -a` para obtener la información más completa sobre los usuarios conectados.
- Si necesitas saber cuándo fue la última vez que se reinició el sistema, `who -b` es muy útil.
- Combina `who` con otros comandos como `grep` para filtrar resultados específicos, por ejemplo, `who | grep username` para buscar un usuario en particular.