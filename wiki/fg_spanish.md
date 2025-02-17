# [Linux] Bash fg Uso equivalente: Traer procesos al primer plano

El comando `fg` se utiliza en Bash para llevar un proceso que se está ejecutando en segundo plano al primer plano, permitiendo interactuar con él directamente.

## Overview
El comando `fg` es útil cuando se ha puesto un proceso en segundo plano y se desea reanudar su ejecución en primer plano. Esto es común en situaciones donde se inician tareas largas y se desea continuar interactuando con ellas.

## Usage
La sintaxis básica del comando `fg` es la siguiente:

```bash
fg [opciones] [número de trabajo]
```

## Common Options
- `número de trabajo`: Especifica el trabajo que se desea llevar al primer plano. Si no se especifica, `fg` traerá el último trabajo en segundo plano.

## Common Examples

1. **Llevar el último trabajo al primer plano:**
   ```bash
   fg
   ```

2. **Llevar un trabajo específico al primer plano:**
   Supongamos que tienes varios trabajos en segundo plano y deseas llevar el trabajo número 1 al primer plano.
   ```bash
   fg %1
   ```

3. **Llevar un trabajo que se ha detenido al primer plano:**
   Si un trabajo fue detenido con `Ctrl + Z`, puedes reanudarlo con:
   ```bash
   fg %2
   ```

## Tips
- Utiliza el comando `jobs` para ver una lista de trabajos en segundo plano y sus números antes de usar `fg`.
- Si necesitas llevar un proceso al primer plano y no quieres perder su estado, asegúrate de que esté detenido antes de usar `fg`.
- Recuerda que puedes usar `Ctrl + Z` para detener un proceso en primer plano y luego usar `fg` para reanudarlo.