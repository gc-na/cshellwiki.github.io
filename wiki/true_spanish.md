# [Linux] Bash true uso equivalente: Comando que siempre devuelve éxito

## Overview
El comando `true` en Bash es una utilidad que no realiza ninguna acción y siempre devuelve un estado de salida exitoso (código de salida 0). Es comúnmente utilizado en scripts para indicar que una operación se ha completado con éxito o para cumplir con la sintaxis de comandos que requieren un comando válido.

## Usage
La sintaxis básica del comando `true` es la siguiente:

```bash
true [opciones]
```

## Common Options
El comando `true` no tiene opciones específicas, ya que su única función es devolver un estado de éxito. Sin embargo, se puede usar en combinación con otras herramientas y comandos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `true`:

1. **Uso en un script simple:**
   ```bash
   #!/bin/bash
   if true; then
       echo "Esto siempre se ejecuta."
   fi
   ```

2. **Usar `true` en un bucle:**
   ```bash
   while true; do
       echo "Este bucle se ejecutará indefinidamente."
       sleep 1
   done
   ```

3. **Combinación con `&&`:**
   ```bash
   true && echo "El comando true se ejecutó con éxito."
   ```

4. **Uso en un comando de prueba:**
   ```bash
   if true; then
       echo "La prueba fue exitosa."
   fi
   ```

## Tips
- Utiliza `true` para crear bucles infinitos que se pueden detener con una condición externa.
- Es útil en scripts para mantener la estructura de control sin realizar ninguna acción.
- Puedes combinar `true` con otros comandos para simplificar la lógica de tus scripts.