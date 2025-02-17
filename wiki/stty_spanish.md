# [Linux] Bash stty Uso: Configuración de terminal

## Overview
El comando `stty` se utiliza para cambiar y mostrar las configuraciones de la terminal. Permite ajustar parámetros como el tamaño de la línea, los caracteres de control y otras opciones que afectan la entrada y salida de datos en la terminal.

## Usage
La sintaxis básica del comando `stty` es la siguiente:

```bash
stty [opciones] [argumentos]
```

## Common Options
- `-a`: Muestra todas las configuraciones actuales de la terminal.
- `-g`: Muestra la configuración actual en un formato que se puede usar posteriormente.
- `erase`: Establece el carácter de borrado (por defecto, suele ser el retroceso).
- `kill`: Establece el carácter de eliminación de línea (por defecto, suele ser Ctrl+U).
- `intr`: Establece el carácter de interrupción (por defecto, suele ser Ctrl+C).

## Common Examples
1. **Mostrar configuraciones actuales:**
   ```bash
   stty -a
   ```

2. **Cambiar el carácter de borrado a `^H`:**
   ```bash
   stty erase ^H
   ```

3. **Establecer el carácter de interrupción a `^C`:**
   ```bash
   stty intr ^C
   ```

4. **Guardar la configuración actual en una variable:**
   ```bash
   config=$(stty -g)
   ```

5. **Restaurar la configuración desde una variable:**
   ```bash
   stty $config
   ```

## Tips
- Siempre verifica la configuración actual con `stty -a` antes de realizar cambios, para evitar configuraciones indeseadas.
- Si cambias la configuración de la terminal y no puedes volver atrás, puedes cerrar la terminal y abrir una nueva para restablecerla a los valores predeterminados.
- Utiliza `stty -g` para guardar la configuración actual antes de hacer cambios, lo que te permitirá restaurarla fácilmente más tarde.