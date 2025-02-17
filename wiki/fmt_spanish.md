# [Linux] Bash fmt Uso: Formatear texto en líneas

## Overview
El comando `fmt` se utiliza para formatear texto en líneas de longitud uniforme. Es útil para preparar texto para su visualización en terminales o para su impresión, asegurando que las líneas no sean demasiado largas.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
fmt [opciones] [archivos]
```

## Common Options
- `-w, --width=N`: Establece el ancho máximo de las líneas a N caracteres. Por defecto, es 75.
- `-s, --split-only`: Solo divide las líneas largas, sin agregar espacios adicionales.
- `-c, --crown`: Alinea el texto en el centro de la línea.

## Common Examples
1. **Formatear un archivo de texto**:
   ```bash
   fmt documento.txt
   ```

2. **Establecer un ancho de línea específico**:
   ```bash
   fmt -w 50 documento.txt
   ```

3. **Dividir líneas largas sin agregar espacios**:
   ```bash
   fmt -s documento.txt
   ```

4. **Alinear texto en el centro**:
   ```bash
   fmt -c documento.txt
   ```

## Tips
- Utiliza `fmt` en combinación con otros comandos como `cat` o `less` para visualizar texto formateado de manera más legible.
- Experimenta con diferentes anchos de línea para encontrar el que mejor se adapte a tus necesidades de visualización.
- Recuerda que `fmt` modifica el texto en la salida estándar, por lo que puedes redirigir la salida a un nuevo archivo si deseas guardar los cambios.