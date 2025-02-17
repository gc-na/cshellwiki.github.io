# [Linux] Bash cmp Uso equivalente: Comparar archivos byte a byte

## Overview
El comando `cmp` se utiliza en sistemas Unix y Linux para comparar dos archivos byte a byte. Su principal función es identificar las diferencias entre los archivos, indicando la primera ubicación donde difieren y, si se desea, también puede mostrar el contenido de las diferencias.

## Usage
La sintaxis básica del comando `cmp` es la siguiente:

```bash
cmp [opciones] [archivo1] [archivo2]
```

## Common Options
- `-l`: Muestra las diferencias en formato de lista, mostrando la posición y los valores octales de los bytes que difieren.
- `-s`: Suprime la salida, solo devuelve el estado de salida.
- `-i OFFSET`: Comienza la comparación a partir de un desplazamiento específico.
- `-n N`: Compara solo los primeros N bytes de los archivos.

## Common Examples

1. **Comparar dos archivos:**
   ```bash
   cmp archivo1.txt archivo2.txt
   ```

2. **Comparar dos archivos y mostrar las diferencias en formato de lista:**
   ```bash
   cmp -l archivo1.txt archivo2.txt
   ```

3. **Comparar dos archivos sin salida, solo estado de salida:**
   ```bash
   cmp -s archivo1.txt archivo2.txt
   ```

4. **Comparar solo los primeros 10 bytes de dos archivos:**
   ```bash
   cmp -n 10 archivo1.txt archivo2.txt
   ```

5. **Comparar archivos comenzando desde un desplazamiento específico:**
   ```bash
   cmp -i 5 archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza la opción `-s` si solo te interesa saber si los archivos son idénticos o no, sin necesidad de ver las diferencias.
- Para archivos grandes, considera usar la opción `-n` para limitar la comparación a un número específico de bytes, lo que puede ahorrar tiempo.
- Si necesitas una comparación más detallada, la opción `-l` es muy útil para obtener información precisa sobre las diferencias.