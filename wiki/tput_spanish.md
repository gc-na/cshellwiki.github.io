# [Linux] Bash tput Uso: Controlar la salida de terminal

## Overview
El comando `tput` se utiliza para controlar la salida en la terminal, permitiendo manipular la apariencia del texto y el comportamiento del terminal. Esto incluye cambiar colores, mover el cursor y limpiar la pantalla, entre otras funcionalidades.

## Usage
La sintaxis básica del comando `tput` es la siguiente:

```bash
tput [opciones] [argumentos]
```

## Common Options
- `clear`: Limpia la pantalla de la terminal.
- `setaf [n]`: Establece el color del texto, donde `[n]` es el número del color (0-7).
- `setab [n]`: Establece el color de fondo, donde `[n]` es el número del color (0-7).
- `cup [y] [x]`: Mueve el cursor a la posición especificada por las coordenadas `[y]` (fila) y `[x]` (columna).
- `bold`: Establece el texto en negrita.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `tput`:

1. **Limpiar la pantalla:**
   ```bash
   tput clear
   ```

2. **Cambiar el color del texto a rojo:**
   ```bash
   tput setaf 1
   echo "Este texto es rojo"
   ```

3. **Cambiar el color de fondo a azul y el texto a blanco:**
   ```bash
   tput setab 4
   tput setaf 7
   echo "Texto con fondo azul y texto blanco"
   ```

4. **Mover el cursor a la posición (5, 10):**
   ```bash
   tput cup 5 10
   echo "Texto en la fila 5, columna 10"
   ```

5. **Establecer texto en negrita:**
   ```bash
   tput bold
   echo "Este texto está en negrita"
   tput sgr0  # Restablece los atributos del texto
   ```

## Tips
- Utiliza `tput sgr0` al final de tus comandos para restablecer los atributos del texto a su estado original.
- Experimenta con diferentes números para `setaf` y `setab` para ver los colores disponibles en tu terminal.
- Combina varios comandos `tput` en un solo script para crear salidas más complejas y visualmente atractivas.