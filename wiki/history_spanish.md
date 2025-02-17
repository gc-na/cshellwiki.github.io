# [Linux] Bash history Uso: Muestra el historial de comandos

## Overview
El comando `history` en Bash se utiliza para mostrar una lista de los comandos que se han ejecutado en la sesión actual del terminal. Esto permite a los usuarios revisar, reutilizar o editar comandos anteriores sin necesidad de volver a escribirlos.

## Usage
La sintaxis básica del comando `history` es la siguiente:

```bash
history [opciones] [número]
```

## Common Options
- `-c`: Borra el historial actual.
- `-d offset`: Elimina la entrada en la posición especificada por `offset`.
- `n`: Muestra las últimas `n` entradas del historial.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `history`:

1. **Mostrar todo el historial de comandos:**
   ```bash
   history
   ```

2. **Mostrar las últimas 10 entradas del historial:**
   ```bash
   history 10
   ```

3. **Eliminar una entrada específica del historial:**
   ```bash
   history -d 5
   ```

4. **Borrar todo el historial:**
   ```bash
   history -c
   ```

5. **Reejecutar un comando del historial:**
   Supongamos que quieres reejecutar el comando en la posición 20:
   ```bash
   !20
   ```

## Tips
- Utiliza `Ctrl + R` para buscar en el historial de comandos de manera interactiva.
- Puedes editar el archivo de historial (`~/.bash_history`) para hacer cambios permanentes.
- Recuerda que el historial se guarda al cerrar la sesión, así que asegúrate de revisar tus comandos antes de salir.