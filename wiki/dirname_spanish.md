# [Linux] Bash dirname Uso: Extraer el nombre del directorio de una ruta

## Overview
El comando `dirname` se utiliza en Bash para extraer el nombre del directorio de una ruta de archivo. Esto es útil cuando se necesita obtener la parte del directorio de una ruta completa, dejando de lado el nombre del archivo.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
dirname [opciones] [argumentos]
```

## Common Options
- **`-z`**: Trata los argumentos como cadenas de longitud cero, lo que permite manejar rutas vacías.
- **`--help`**: Muestra la ayuda sobre el uso del comando.
- **`--version`**: Muestra la versión del comando `dirname`.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `dirname`:

1. **Obtener el directorio de un archivo específico:**
   ```bash
   dirname /home/usuario/documentos/archivo.txt
   ```
   Salida:
   ```
   /home/usuario/documentos
   ```

2. **Extraer el directorio de una ruta relativa:**
   ```bash
   dirname ./proyectos/codigo.py
   ```
   Salida:
   ```
   ./proyectos
   ```

3. **Usar dirname en combinación con otros comandos:**
   ```bash
   dirname $(pwd)/archivo.txt
   ```
   Salida:
   ```
   /ruta/actual
   ```

4. **Manejo de rutas vacías:**
   ```bash
   dirname ""
   ```
   Salida:
   ```
   .
   ```

## Tips
- Utiliza `dirname` en scripts para manejar rutas de archivos de manera más eficiente.
- Combina `dirname` con otros comandos como `basename` para manipular rutas de archivo de manera más efectiva.
- Recuerda que `dirname` siempre devuelve el directorio que contiene el archivo, así que asegúrate de que la ruta proporcionada sea válida.