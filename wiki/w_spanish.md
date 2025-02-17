# [Linux] Bash w: [muestra quién está conectado]

## Overview
El comando `w` en Bash se utiliza para mostrar información sobre los usuarios que están actualmente conectados al sistema. Proporciona detalles como el nombre de usuario, el terminal, la hora de inicio de sesión, el tiempo de inactividad y el comando que están ejecutando.

## Usage
La sintaxis básica del comando `w` es la siguiente:

```bash
w [opciones] [argumentos]
```

## Common Options
- `-h`: Omite la línea de encabezado.
- `-s`: Muestra una salida más concisa.
- `-u`: Muestra el tiempo de inactividad de los usuarios.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `w`:

1. **Mostrar usuarios conectados:**
   ```bash
   w
   ```

2. **Mostrar usuarios conectados sin encabezado:**
   ```bash
   w -h
   ```

3. **Mostrar salida concisa:**
   ```bash
   w -s
   ```

4. **Mostrar usuarios conectados con tiempo de inactividad:**
   ```bash
   w -u
   ```

## Tips
- Utiliza `w` regularmente para monitorear la actividad de los usuarios en sistemas compartidos.
- Combina `w` con otros comandos como `grep` para filtrar resultados específicos.
- Recuerda que la información mostrada puede variar según los permisos del usuario que ejecute el comando.