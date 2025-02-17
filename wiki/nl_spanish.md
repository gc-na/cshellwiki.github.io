# [Linux] Bash nl Uso equivalente: Numerar líneas en un archivo de texto

## Overview
El comando `nl` se utiliza en Bash para numerar las líneas de un archivo de texto. Este comando es útil para agregar números de línea a la salida, lo que facilita la referencia a líneas específicas en documentos largos.

## Usage
La sintaxis básica del comando `nl` es la siguiente:

```bash
nl [opciones] [argumentos]
```

## Common Options
- `-b`: Define el tipo de numeración de líneas. Puede ser `a` (numerar todas las líneas), `t` (numerar solo líneas no vacías) o `n` (no numerar).
- `-f`: Especifica el número de líneas que se omiten antes de comenzar la numeración.
- `-h`: Permite agregar un encabezado antes de la numeración.
- `-v`: Establece el número inicial para la numeración de líneas.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `nl`:

1. **Numerar todas las líneas de un archivo:**
   ```bash
   nl archivo.txt
   ```

2. **Numerar solo líneas no vacías:**
   ```bash
   nl -b t archivo.txt
   ```

3. **Comenzar la numeración desde un número específico:**
   ```bash
   nl -v 100 archivo.txt
   ```

4. **Agregar un encabezado a la salida:**
   ```bash
   nl -h "Encabezado de ejemplo" archivo.txt
   ```

5. **Omitir las primeras 5 líneas antes de numerar:**
   ```bash
   nl -f 5 archivo.txt
   ```

## Tips
- Utiliza `nl` en combinación con otros comandos, como `cat`, para visualizar archivos numerados de manera rápida.
- Puedes redirigir la salida de `nl` a un nuevo archivo usando `>` para guardar el resultado.
- Experimenta con diferentes opciones para personalizar la numeración según tus necesidades específicas.