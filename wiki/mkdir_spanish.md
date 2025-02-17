# [Linux] Bash mkdir Uso: Crear directorios en el sistema de archivos

## Overview
El comando `mkdir` se utiliza en Bash para crear nuevos directorios en el sistema de archivos. Es una herramienta fundamental para organizar archivos y carpetas de manera efectiva.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
mkdir [opciones] [argumentos]
```

## Common Options
- `-p`: Crea directorios padres según sea necesario. Si los directorios intermedios no existen, los crea automáticamente.
- `-v`: Muestra un mensaje por cada directorio que se crea, lo que puede ser útil para verificar la creación de directorios.
- `-m`: Establece los permisos del nuevo directorio al momento de su creación, utilizando la notación octal.

## Common Examples
1. **Crear un solo directorio:**
   ```bash
   mkdir mi_directorio
   ```

2. **Crear varios directorios a la vez:**
   ```bash
   mkdir directorio1 directorio2 directorio3
   ```

3. **Crear un directorio y sus padres si no existen:**
   ```bash
   mkdir -p ruta/a/mi_directorio
   ```

4. **Crear un directorio y mostrar un mensaje:**
   ```bash
   mkdir -v nuevo_directorio
   ```

5. **Crear un directorio con permisos específicos:**
   ```bash
   mkdir -m 755 mi_directorio
   ```

## Tips
- Utiliza la opción `-p` cuando no estés seguro si los directorios intermedios existen; esto evitará errores.
- Revisa los permisos de los directorios creados con `ls -l` para asegurarte de que son los deseados.
- Considera usar nombres descriptivos para tus directorios, lo que facilitará la organización y búsqueda de archivos en el futuro.