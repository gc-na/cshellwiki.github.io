# [Linux] Bash pr: Formatear archivos de texto para impresión

## Overview
El comando `pr` se utiliza en sistemas Unix y Linux para formatear archivos de texto de manera que sean más fáciles de leer al imprimir. Este comando organiza el contenido en columnas y agrega encabezados y pies de página, lo que resulta útil para la presentación de documentos.

## Usage
La sintaxis básica del comando `pr` es la siguiente:

```bash
pr [opciones] [argumentos]
```

## Common Options
- `-h, --header=STRING`: Especifica un encabezado personalizado para la salida.
- `-f, --form-feed`: Imprime un salto de página antes de cada archivo.
- `-t, --omit-header`: Omite el encabezado de la salida.
- `-s, --separator=STRING`: Define un separador personalizado entre columnas.
- `-w, --width=N`: Establece el ancho de la salida en N caracteres.

## Common Examples
1. **Formatear un archivo de texto simple:**
   ```bash
   pr archivo.txt
   ```

2. **Agregar un encabezado personalizado:**
   ```bash
   pr -h "Mi Encabezado" archivo.txt
   ```

3. **Imprimir múltiples archivos con salto de página:**
   ```bash
   pr -f archivo1.txt archivo2.txt
   ```

4. **Omitir el encabezado y establecer un ancho específico:**
   ```bash
   pr -t -w 80 archivo.txt
   ```

5. **Separar columnas con un carácter específico:**
   ```bash
   pr -s "," archivo.txt
   ```

## Tips
- Utiliza la opción `-w` para ajustar el ancho de la salida según el tamaño del papel que vayas a utilizar.
- Si estás imprimiendo varios archivos, considera usar la opción `-f` para mejorar la legibilidad.
- Experimenta con diferentes separadores utilizando la opción `-s` para ver cuál se adapta mejor a tus necesidades.