# [Linux] Bash md5sum Uso: Calcular y verificar sumas de verificación MD5

## Overview
El comando `md5sum` se utiliza para calcular y verificar la suma de verificación MD5 de archivos. Esta suma de verificación es un valor hash que se genera a partir del contenido del archivo, lo que permite comprobar la integridad de los datos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
md5sum [opciones] [argumentos]
```

## Common Options
- `-b`: Procesa archivos binarios.
- `-c`: Verifica las sumas de verificación de un archivo.
- `-t`: Calcula la suma de verificación de un archivo de texto.
- `--help`: Muestra la ayuda sobre el uso del comando.
- `--version`: Muestra la versión del comando.

## Common Examples
1. **Calcular la suma de verificación de un archivo:**
   ```bash
   md5sum archivo.txt
   ```

2. **Guardar la suma de verificación en un archivo:**
   ```bash
   md5sum archivo.txt > checksum.md5
   ```

3. **Verificar la suma de verificación desde un archivo:**
   ```bash
   md5sum -c checksum.md5
   ```

4. **Calcular la suma de verificación de varios archivos:**
   ```bash
   md5sum archivo1.txt archivo2.txt
   ```

## Tips
- Siempre guarda las sumas de verificación en un archivo separado para facilitar la verificación posterior.
- Utiliza el comando `-c` para verificar la integridad de los archivos después de transferencias o copias.
- Recuerda que MD5 no es adecuado para aplicaciones de seguridad críticas, ya que se ha demostrado que es vulnerable a colisiones. Considera usar algoritmos más seguros como SHA-256 si es necesario.