# [Linux] Bash sleep Uso: Pausar la ejecución de un script

## Overview
El comando `sleep` se utiliza en Bash para pausar la ejecución de un script o un comando durante un período de tiempo específico. Esto es útil en diversas situaciones, como cuando se necesita esperar antes de ejecutar la siguiente acción o para crear intervalos entre comandos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
sleep [opciones] [tiempo]
```

Donde `[tiempo]` puede especificarse en segundos, minutos, horas o días.

## Common Options
- `-h`, `--help`: Muestra la ayuda del comando.
- `-V`, `--version`: Muestra la versión del comando `sleep`.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `sleep`:

1. **Pausar por 5 segundos:**
   ```bash
   sleep 5
   ```

2. **Pausar por 2 minutos:**
   ```bash
   sleep 2m
   ```

3. **Pausar por 1 hora:**
   ```bash
   sleep 1h
   ```

4. **Pausar por 1 día:**
   ```bash
   sleep 1d
   ```

5. **Usar `sleep` en un bucle:**
   ```bash
   for i in {1..5}; do
       echo "Contador: $i"
       sleep 1
   done
   ```

## Tips
- Utiliza `sleep` en scripts automatizados para evitar sobrecargar el sistema con múltiples procesos simultáneos.
- Combina `sleep` con otros comandos en un script para crear pausas entre tareas, lo que puede ser útil para la depuración.
- Recuerda que el tiempo puede expresarse en diferentes unidades, lo que te permite ajustar fácilmente la duración de la pausa según tus necesidades.