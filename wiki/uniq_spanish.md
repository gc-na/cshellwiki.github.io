# [Linux] Bash uniq Uso equivalente: Eliminar líneas duplicadas en un archivo

## Overview
El comando `uniq` se utiliza en Bash para filtrar líneas duplicadas en un archivo o en la entrada estándar. Es especialmente útil cuando se desea obtener una lista de elementos únicos a partir de un conjunto de datos.

## Usage
La sintaxis básica del comando `uniq` es la siguiente:

```bash
uniq [opciones] [archivo]
```

## Common Options
- `-c`: Cuenta el número de ocurrencias de cada línea y muestra el conteo junto a la línea.
- `-d`: Muestra solo las líneas que están duplicadas.
- `-u`: Muestra solo las líneas que son únicas (no duplicadas).
- `-i`: Ignora las diferencias entre mayúsculas y minúsculas al comparar líneas.

## Common Examples
1. **Eliminar líneas duplicadas de un archivo:**
   ```bash
   uniq archivo.txt
   ```

2. **Contar las ocurrencias de cada línea:**
   ```bash
   uniq -c archivo.txt
   ```

3. **Mostrar solo líneas duplicadas:**
   ```bash
   uniq -d archivo.txt
   ```

4. **Mostrar solo líneas únicas:**
   ```bash
   uniq -u archivo.txt
   ```

5. **Ignorar mayúsculas y minúsculas:**
   ```bash
   uniq -i archivo.txt
   ```

## Tips
- Asegúrate de que el archivo de entrada esté ordenado, ya que `uniq` solo elimina duplicados adyacentes. Puedes usar el comando `sort` antes de `uniq` para ordenar el archivo.
- Para procesar la entrada estándar, puedes usar `echo` o redirigir la salida de otro comando:
  ```bash
  echo -e "a\nb\na\nc\nb" | sort | uniq
  ```
- Combina `uniq` con otros comandos de Unix para crear potentes tuberías de procesamiento de texto.