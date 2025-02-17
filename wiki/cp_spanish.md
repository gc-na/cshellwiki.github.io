# [Linux] Bash cp Uso: Copiar archivos y directorios

## Overview
El comando `cp` se utiliza en Bash para copiar archivos y directorios de un lugar a otro en el sistema de archivos. Es una herramienta fundamental para la gestión de archivos en entornos Unix y Linux.

## Usage
La sintaxis básica del comando `cp` es la siguiente:

```bash
cp [opciones] [origen] [destino]
```

## Common Options
- `-r`: Copia directorios de forma recursiva.
- `-i`: Pregunta antes de sobrescribir archivos existentes.
- `-u`: Copia solo si el archivo de origen es más reciente que el archivo de destino o si el archivo de destino no existe.
- `-v`: Muestra el progreso de la copia en la terminal.
- `-a`: Copia archivos y directorios de manera que se preserven las propiedades (modo, propietario, timestamps, etc.).

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `cp`:

1. **Copiar un archivo a otro directorio:**
   ```bash
   cp archivo.txt /ruta/al/destino/
   ```

2. **Copiar un directorio de forma recursiva:**
   ```bash
   cp -r directorio/ /ruta/al/destino/
   ```

3. **Copiar un archivo y preguntar antes de sobrescribir:**
   ```bash
   cp -i archivo.txt /ruta/al/destino/
   ```

4. **Copiar solo archivos más recientes:**
   ```bash
   cp -u archivo.txt /ruta/al/destino/
   ```

5. **Copiar un archivo y mostrar el progreso:**
   ```bash
   cp -v archivo.txt /ruta/al/destino/
   ```

## Tips
- Siempre verifica el destino antes de realizar copias, especialmente cuando usas la opción `-i` para evitar sobrescribir archivos importantes.
- Utiliza la opción `-a` cuando necesites hacer una copia de seguridad completa de un directorio, ya que preserva todos los atributos del archivo.
- Si copias archivos grandes o muchos archivos, considera usar `rsync` para una copia más eficiente y con más opciones de control.