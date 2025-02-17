# [Linux] Bash echo uso equivalente: Muestra texto en la salida estándar

## Overview
El comando `echo` en Bash se utiliza para mostrar texto o variables en la salida estándar. Es una herramienta fundamental para la visualización de información en scripts y en la línea de comandos.

## Usage
La sintaxis básica del comando `echo` es la siguiente:

```bash
echo [opciones] [argumentos]
```

## Common Options
- `-n`: No imprime una nueva línea al final.
- `-e`: Activa la interpretación de caracteres especiales como `\n` (nueva línea) y `\t` (tabulación).
- `-E`: Desactiva la interpretación de caracteres especiales (por defecto).

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `echo`:

1. Mostrar un simple mensaje:
   ```bash
   echo "Hola, mundo!"
   ```

2. Mostrar el valor de una variable:
   ```bash
   nombre="Juan"
   echo "Hola, $nombre!"
   ```

3. Usar la opción `-n` para evitar una nueva línea:
   ```bash
   echo -n "Este texto no tiene nueva línea al final."
   ```

4. Usar la opción `-e` para interpretar caracteres especiales:
   ```bash
   echo -e "Primera línea\nSegunda línea"
   ```

5. Mostrar texto con tabulaciones:
   ```bash
   echo -e "Columna1\tColumna2\tColumna3"
   ```

## Tips
- Siempre verifica si necesitas la opción `-n` para evitar nuevas líneas, especialmente en scripts.
- Usa `-e` si necesitas mostrar caracteres especiales, pero ten en cuenta que no todos los sistemas tienen esta opción habilitada por defecto.
- Puedes redirigir la salida de `echo` a un archivo utilizando `>`:
  ```bash
  echo "Este texto se guardará en un archivo." > archivo.txt
  ```