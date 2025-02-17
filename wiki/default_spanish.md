# [Linux] Bash default uso: Comando para mostrar el contenido de archivos

## Overview
El comando `cat` se utiliza en Bash para concatenar y mostrar el contenido de uno o más archivos en la salida estándar. Es una herramienta fundamental para visualizar rápidamente el contenido de archivos de texto.

## Usage
La sintaxis básica del comando `cat` es la siguiente:

```bash
cat [opciones] [archivos]
```

## Common Options
- `-n`: Numera todas las líneas de la salida.
- `-b`: Numera solo las líneas no vacías.
- `-E`: Muestra el símbolo `$` al final de cada línea.
- `-s`: Suprime las líneas vacías consecutivas.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `cat`:

1. **Mostrar el contenido de un archivo**:
   ```bash
   cat archivo.txt
   ```

2. **Concatenar y mostrar el contenido de varios archivos**:
   ```bash
   cat archivo1.txt archivo2.txt
   ```

3. **Numerar todas las líneas de un archivo**:
   ```bash
   cat -n archivo.txt
   ```

4. **Suprimir líneas vacías consecutivas**:
   ```bash
   cat -s archivo.txt
   ```

5. **Mostrar el contenido de un archivo y agregar un símbolo al final de cada línea**:
   ```bash
   cat -E archivo.txt
   ```

## Tips
- Utiliza `cat` en combinación con otros comandos, como `grep`, para filtrar el contenido mostrado.
- Para archivos muy grandes, considera usar `less` o `more` en lugar de `cat` para una visualización más controlada.
- Recuerda que `cat` puede ser utilizado para crear archivos nuevos al redirigir la salida, por ejemplo:
  ```bash
  cat > nuevo_archivo.txt
  ``` 
  Luego puedes escribir el contenido y finalizar con `Ctrl + D`.