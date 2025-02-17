# [Linux] Bash tmux Uso: Multiplexor de terminales

## Overview
El comando `tmux` es un multiplexor de terminales que permite a los usuarios gestionar múltiples sesiones de terminal dentro de una sola ventana. Esto es especialmente útil para mantener procesos en ejecución incluso si se desconecta de la sesión SSH o si se necesita trabajar en varias tareas simultáneamente.

## Usage
La sintaxis básica del comando `tmux` es la siguiente:

```bash
tmux [opciones] [argumentos]
```

## Common Options
- `new`: Crea una nueva sesión de tmux.
- `attach`: Se conecta a una sesión existente.
- `list-sessions`: Muestra todas las sesiones de tmux activas.
- `kill-session`: Termina una sesión específica.
- `detach`: Desconecta la sesión actual, dejándola en segundo plano.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `tmux`:

1. **Crear una nueva sesión:**
   ```bash
   tmux new -s mi_sesion
   ```

2. **Adjuntarse a una sesión existente:**
   ```bash
   tmux attach -t mi_sesion
   ```

3. **Listar todas las sesiones activas:**
   ```bash
   tmux list-sessions
   ```

4. **Desconectar de la sesión actual:**
   Presiona `Ctrl + b`, luego `d`.

5. **Terminar una sesión específica:**
   ```bash
   tmux kill-session -t mi_sesion
   ```

## Tips
- Usa `Ctrl + b` seguido de `?` para ver una lista de atajos de teclado disponibles en tmux.
- Organiza tu trabajo en paneles divididos usando `Ctrl + b`, luego `%` para dividir verticalmente o `"` para dividir horizontalmente.
- Guarda tus sesiones de tmux para reanudarlas más tarde, lo que te permite continuar trabajando sin perder el progreso.