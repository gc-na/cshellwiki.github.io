# [Linux] Bash mv Uso: Mover o renombrar archivos y directorios

## Overview
El comando `mv` se utiliza en Bash para mover o renombrar archivos y directorios. Es una herramienta fundamental para la gestión de archivos en sistemas operativos basados en Unix.

## Usage
La sintaxis básica del comando `mv` es la siguiente:

```bash
mv [opciones] [origen] [destino]
```

## Common Options
- `-i`: Pregunta antes de sobrescribir un archivo existente.
- `-u`: Mueve el archivo solo si el archivo de origen es más nuevo que el archivo de destino o si el archivo de destino no existe.
- `-v`: Muestra información detallada sobre lo que está haciendo el comando.
- `-n`: No sobrescribe archivos existentes.

## Common Examples
1. **Mover un archivo a otro directorio:**
   ```bash
   mv archivo.txt /ruta/al/nuevo/directorio/
   ```

2. **Renombrar un archivo:**
   ```bash
   mv viejo_nombre.txt nuevo_nombre.txt
   ```

3. **Mover varios archivos a un directorio:**
   ```bash
   mv archivo1.txt archivo2.txt /ruta/al/nuevo/directorio/
   ```

4. **Mover un directorio completo:**
   ```bash
   mv /ruta/al/directorio /ruta/al/nuevo/directorio/
   ```

5. **Mover un archivo y preguntar antes de sobrescribir:**
   ```bash
   mv -i archivo.txt /ruta/al/nuevo/directorio/
   ```

## Tips
- Siempre verifica el destino antes de mover archivos para evitar pérdidas de datos.
- Utiliza la opción `-v` para tener un seguimiento claro de las operaciones que estás realizando.
- Si no estás seguro de lo que hará el comando, prueba primero con la opción `-i` para evitar sobrescribir archivos accidentalmente.