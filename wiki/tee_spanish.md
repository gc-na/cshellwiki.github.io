# [Linux] Bash tee Uso: Redirigir la salida a archivos y a la pantalla

## Overview
El comando `tee` en Bash se utiliza para leer la entrada estándar y escribirla simultáneamente en la salida estándar y en uno o más archivos. Esto permite que los usuarios vean la salida de un comando en la terminal mientras también la guardan en un archivo.

## Usage
La sintaxis básica del comando `tee` es la siguiente:

```bash
tee [opciones] [archivos]
```

## Common Options
- `-a`, `--append`: Añade la salida al final de los archivos en lugar de sobrescribirlos.
- `-i`, `--ignore-interrupts`: Ignora las señales de interrupción.
- `--help`: Muestra la ayuda sobre el comando `tee`.
- `--version`: Muestra la versión del comando `tee`.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `tee`:

1. **Guardar la salida de un comando en un archivo:**
   ```bash
   ls -l | tee listado.txt
   ```
   Este comando lista los archivos en el directorio actual y guarda la salida en `listado.txt`.

2. **Añadir la salida a un archivo existente:**
   ```bash
   echo "Nueva línea" | tee -a listado.txt
   ```
   Aquí, se añade "Nueva línea" al final del archivo `listado.txt`.

3. **Ver la salida en la terminal y en múltiples archivos:**
   ```bash
   echo "Hola, mundo" | tee archivo1.txt archivo2.txt
   ```
   Este comando muestra "Hola, mundo" en la terminal y lo guarda tanto en `archivo1.txt` como en `archivo2.txt`.

4. **Usar tee con un comando que genera mucha salida:**
   ```bash
   dmesg | tee dmesg_output.txt
   ```
   Este comando guarda la salida del registro del núcleo en `dmesg_output.txt` mientras la muestra en la terminal.

## Tips
- Utiliza la opción `-a` si deseas agregar contenido a un archivo existente sin perder lo que ya hay.
- Combina `tee` con otros comandos en una tubería para capturar la salida mientras la visualizas.
- Recuerda que `tee` puede ser útil para depurar scripts, ya que te permite ver la salida de cada paso en el proceso.