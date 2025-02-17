# [Linux] Bash sort uso equivalente en español: Ordenar líneas de texto

## Overview
El comando `sort` se utiliza en Bash para ordenar líneas de texto en archivos o en la entrada estándar. Permite organizar datos de manera ascendente o descendente, facilitando la visualización y el análisis de información.

## Usage
La sintaxis básica del comando `sort` es la siguiente:

```bash
sort [opciones] [argumentos]
```

## Common Options
Aquí hay algunas opciones comunes que se pueden utilizar con el comando `sort`:

- `-r`: Ordenar en orden descendente.
- `-n`: Ordenar numéricamente.
- `-k`: Especificar la clave de ordenación (por ejemplo, la columna).
- `-u`: Eliminar líneas duplicadas.
- `-o`: Especificar un archivo de salida para guardar el resultado.

## Common Examples
A continuación se presentan algunos ejemplos prácticos del uso del comando `sort`:

1. **Ordenar un archivo de texto en orden ascendente:**
   ```bash
   sort archivo.txt
   ```

2. **Ordenar un archivo en orden descendente:**
   ```bash
   sort -r archivo.txt
   ```

3. **Ordenar numéricamente:**
   ```bash
   sort -n numeros.txt
   ```

4. **Ordenar por la segunda columna:**
   ```bash
   sort -k2 archivo.txt
   ```

5. **Eliminar líneas duplicadas y ordenar:**
   ```bash
   sort -u archivo.txt
   ```

6. **Guardar el resultado en un nuevo archivo:**
   ```bash
   sort archivo.txt -o archivo_ordenado.txt
   ```

## Tips
- Siempre verifica el contenido del archivo original antes de aplicar `sort`, especialmente si usas la opción `-o`, ya que sobrescribirá el archivo de salida.
- Combina `sort` con otros comandos como `uniq` para obtener resultados más específicos, por ejemplo, `sort archivo.txt | uniq`.
- Usa `man sort` para acceder a la página de manual y explorar más opciones y detalles sobre el comando.