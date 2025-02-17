# [Linux] Bash comm uso: Comparar líneas de archivos

## Overview
El comando `comm` se utiliza para comparar dos archivos de texto ordenados línea por línea. Este comando muestra las líneas que son únicas para cada archivo y las líneas que son comunes a ambos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
comm [opciones] [archivo1] [archivo2]
```

## Common Options
- `-1`: Suprime las líneas que son únicas para el primer archivo.
- `-2`: Suprime las líneas que son únicas para el segundo archivo.
- `-3`: Suprime las líneas que son comunes a ambos archivos.
- `--nocheck-order`: Permite comparar archivos que no están ordenados.

## Common Examples

### Comparar dos archivos
Para comparar dos archivos y ver todas las líneas, puedes usar:

```bash
comm archivo1.txt archivo2.txt
```

### Suprimir líneas únicas del primer archivo
Si solo deseas ver las líneas que son comunes y las del segundo archivo, puedes usar:

```bash
comm -13 archivo1.txt archivo2.txt
```

### Suprimir líneas comunes
Para ver solo las líneas únicas de cada archivo, puedes usar:

```bash
comm -12 archivo1.txt archivo2.txt
```

### Comparar archivos no ordenados
Si los archivos no están ordenados, puedes usar la opción `--nocheck-order`:

```bash
comm --nocheck-order archivo1.txt archivo2.txt
```

## Tips
- Asegúrate de que los archivos estén ordenados antes de usar `comm` para obtener resultados precisos.
- Puedes usar `sort` en combinación con `comm` para ordenar los archivos automáticamente:

```bash
comm <(sort archivo1.txt) <(sort archivo2.txt)
```
- Utiliza las opciones adecuadas para filtrar la salida según tus necesidades específicas.