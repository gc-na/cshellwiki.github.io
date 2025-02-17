# [Linux] Bash sha256sum Uso: Calcular y verificar sumas de verificación SHA-256

## Overview
El comando `sha256sum` se utiliza para calcular y verificar la suma de verificación SHA-256 de archivos. Esta suma de verificación es una representación única del contenido del archivo, lo que permite detectar cambios o corrupciones en los datos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
sha256sum [opciones] [argumentos]
```

## Common Options
- `-b`, `--binary`: Procesa el archivo en modo binario.
- `-c`, `--check`: Verifica las sumas de verificación de los archivos listados en un archivo.
- `-h`, `--help`: Muestra la ayuda y la información sobre el uso del comando.
- `-o`, `--output`: Especifica un archivo de salida para las sumas de verificación.

## Common Examples
1. **Calcular la suma de verificación de un archivo:**
   ```bash
   sha256sum archivo.txt
   ```

2. **Guardar la suma de verificación en un archivo:**
   ```bash
   sha256sum archivo.txt > suma.txt
   ```

3. **Verificar la suma de verificación usando un archivo de suma:**
   ```bash
   sha256sum -c suma.txt
   ```

4. **Calcular la suma de verificación de varios archivos:**
   ```bash
   sha256sum archivo1.txt archivo2.txt
   ```

5. **Calcular la suma de verificación en modo binario:**
   ```bash
   sha256sum -b archivo.bin
   ```

## Tips
- Siempre verifica las sumas de verificación después de transferir archivos importantes para asegurar que no se hayan corrompido.
- Utiliza el modo binario para archivos no de texto para obtener resultados precisos.
- Mantén un registro de las sumas de verificación en un archivo separado para facilitar la verificación futura.