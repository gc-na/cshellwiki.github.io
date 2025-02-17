# [Linux] Bash curl uso: Herramienta para transferir datos desde o hacia un servidor

## Overview
El comando `curl` es una herramienta de línea de comandos utilizada para transferir datos desde o hacia un servidor. Soporta múltiples protocolos, incluyendo HTTP, HTTPS, FTP y más. Es especialmente útil para realizar solicitudes web y descargar archivos.

## Usage
La sintaxis básica del comando `curl` es la siguiente:

```bash
curl [opciones] [argumentos]
```

## Common Options
Aquí hay algunas opciones comunes que puedes usar con `curl`:

- `-X`: Especifica el método HTTP a utilizar (GET, POST, PUT, DELETE, etc.).
- `-d`: Envía datos en una solicitud POST.
- `-H`: Agrega un encabezado HTTP a la solicitud.
- `-o`: Guarda la salida en un archivo en lugar de mostrarla en la consola.
- `-I`: Obtiene solo los encabezados de la respuesta.

## Common Examples
A continuación, se presentan algunos ejemplos prácticos del uso de `curl`:

1. **Realizar una solicitud GET simple:**
   ```bash
   curl https://www.ejemplo.com
   ```

2. **Descargar un archivo y guardarlo con un nombre específico:**
   ```bash
   curl -o archivo.txt https://www.ejemplo.com/archivo.txt
   ```

3. **Enviar datos en una solicitud POST:**
   ```bash
   curl -X POST -d "nombre=Juan&edad=30" https://www.ejemplo.com/api
   ```

4. **Agregar un encabezado a la solicitud:**
   ```bash
   curl -H "Authorization: Bearer token" https://www.ejemplo.com/api/protegida
   ```

5. **Obtener solo los encabezados de la respuesta:**
   ```bash
   curl -I https://www.ejemplo.com
   ```

## Tips
- Siempre verifica la URL antes de realizar una solicitud para evitar errores.
- Usa la opción `-v` para habilitar el modo verbose y obtener más detalles sobre la solicitud y la respuesta.
- Si trabajas con APIs, consulta la documentación de la API para conocer los métodos y parámetros disponibles.
- Considera usar `curl` junto con herramientas como `jq` para procesar respuestas JSON de manera más efectiva.