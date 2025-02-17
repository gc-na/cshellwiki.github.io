# [Linux] Bash ps Uso equivalente: Muestra información sobre procesos en ejecución

## Overview
El comando `ps` se utiliza en sistemas Unix y Linux para mostrar información sobre los procesos en ejecución. Permite a los usuarios ver qué procesos están activos, así como detalles como el uso de CPU, memoria y el estado de cada proceso.

## Usage
La sintaxis básica del comando `ps` es la siguiente:

```bash
ps [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes del comando `ps`:

- `-e` o `-A`: Muestra todos los procesos en el sistema.
- `-f`: Muestra información completa sobre los procesos, incluyendo el usuario, PID, y el comando completo.
- `-u [usuario]`: Muestra los procesos de un usuario específico.
- `-aux`: Muestra todos los procesos con detalles adicionales, incluyendo procesos de otros usuarios.
- `--sort`: Permite ordenar la salida según un criterio específico, como el uso de memoria o CPU.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `ps`:

1. Mostrar todos los procesos en ejecución:
   ```bash
   ps -e
   ```

2. Mostrar todos los procesos con información completa:
   ```bash
   ps -ef
   ```

3. Mostrar los procesos de un usuario específico:
   ```bash
   ps -u nombre_usuario
   ```

4. Mostrar todos los procesos con detalles adicionales:
   ```bash
   ps aux
   ```

5. Ordenar los procesos por uso de memoria:
   ```bash
   ps aux --sort=-%mem
   ```

## Tips
- Utiliza `ps aux` para obtener una vista completa de todos los procesos, incluyendo los de otros usuarios.
- Combina `ps` con otros comandos como `grep` para filtrar resultados. Por ejemplo, para encontrar procesos relacionados con "apache":
  ```bash
  ps aux | grep apache
  ```
- Recuerda que `ps` muestra una instantánea de los procesos en el momento en que se ejecuta. Para monitorear procesos en tiempo real, considera usar `top` o `htop`.