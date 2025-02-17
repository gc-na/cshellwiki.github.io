# [Linux] Bash bg Uso equivalente: Mover trabajos a segundo plano

El comando `bg` se utiliza en Bash para reanudar un trabajo suspendido y moverlo a segundo plano, permitiendo que continúe su ejecución mientras se pueden realizar otras tareas en la terminal.

## Overview
El comando `bg` es útil cuando se ha suspendido un proceso (por ejemplo, presionando `Ctrl+Z`) y se desea que continúe ejecutándose en segundo plano. Esto permite liberar la terminal para otros comandos mientras el proceso sigue activo.

## Usage
La sintaxis básica del comando `bg` es la siguiente:

```bash
bg [opciones] [número del trabajo]
```

## Common Options
- `-n`: No muestra mensajes de estado.
- `-p`: Muestra el PID del trabajo en segundo plano.

## Common Examples

1. **Reanudar el último trabajo suspendido en segundo plano:**
   ```bash
   bg
   ```

2. **Reanudar un trabajo específico en segundo plano:**
   Supongamos que tienes un trabajo suspendido con el número de trabajo 1:
   ```bash
   bg %1
   ```

3. **Reanudar un trabajo en segundo plano sin mostrar mensajes:**
   ```bash
   bg -n %1
   ```

4. **Verificar el estado de los trabajos:**
   Antes de usar `bg`, puedes listar los trabajos suspendidos con:
   ```bash
   jobs
   ```

## Tips
- Siempre verifica los trabajos suspendidos con `jobs` antes de usar `bg` para asegurarte de que estás reanudando el correcto.
- Recuerda que los trabajos en segundo plano pueden generar salida en la terminal, lo que puede interferir con otros comandos. Considera redirigir la salida si es necesario.
- Utiliza `fg` si necesitas llevar un trabajo de nuevo al primer plano en cualquier momento.