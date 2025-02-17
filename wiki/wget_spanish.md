# [Linux] Bash wget Uso: Descarga archivos desde la web

## Overview
El comando `wget` es una herramienta de línea de comandos utilizada para descargar archivos desde la web. Es especialmente útil para descargar contenido de forma no interactiva, lo que significa que puede ejecutarse en segundo plano y continuar la descarga incluso si se cierra la sesión.

## Usage
La sintaxis básica del comando `wget` es la siguiente:

```bash
wget [opciones] [URL]
```

## Common Options
A continuación, se presentan algunas opciones comunes que se pueden utilizar con `wget`:

- `-O [archivo]`: Especifica el nombre del archivo de salida.
- `-c`: Continúa una descarga interrumpida.
- `-r`: Descarga recursivamente archivos de un sitio web.
- `--limit-rate=[velocidad]`: Limita la velocidad de descarga a la cantidad especificada.
- `-q`: Ejecuta el comando en modo silencioso, sin mostrar mensajes.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `wget`:

1. **Descargar un archivo simple:**
   ```bash
   wget https://ejemplo.com/archivo.zip
   ```

2. **Descargar un archivo y guardarlo con un nombre específico:**
   ```bash
   wget -O nuevo_nombre.zip https://ejemplo.com/archivo.zip
   ```

3. **Continuar una descarga interrumpida:**
   ```bash
   wget -c https://ejemplo.com/archivo.zip
   ```

4. **Descargar un sitio web de forma recursiva:**
   ```bash
   wget -r https://ejemplo.com
   ```

5. **Limitar la velocidad de descarga:**
   ```bash
   wget --limit-rate=200k https://ejemplo.com/archivo.zip
   ```

## Tips
- Siempre verifica la URL antes de descargar para asegurarte de que es segura.
- Usa la opción `-q` si deseas ejecutar descargas en scripts sin mostrar información innecesaria.
- Considera usar `-r` con cuidado, ya que puede descargar una gran cantidad de datos y afectar el servidor de origen.