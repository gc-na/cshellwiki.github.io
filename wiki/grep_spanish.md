# [Linux] Bash grep uso equivalente: Buscar texto en archivos

## Overview
El comando `grep` se utiliza para buscar texto dentro de archivos. Permite encontrar líneas que coinciden con un patrón específico, lo que lo convierte en una herramienta muy útil para la manipulación y análisis de texto en la línea de comandos.

## Usage
La sintaxis básica del comando `grep` es la siguiente:

```bash
grep [opciones] [patrón] [archivo]
```

## Common Options
- `-i`: Ignorar mayúsculas y minúsculas al buscar.
- `-r`: Buscar recursivamente en directorios.
- `-v`: Invertir la búsqueda, mostrando líneas que no coinciden con el patrón.
- `-n`: Mostrar el número de línea junto con las coincidencias.
- `-l`: Listar solo los nombres de los archivos que contienen el patrón.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `grep`:

### Buscar una palabra en un archivo
```bash
grep "palabra" archivo.txt
```

### Buscar sin distinguir entre mayúsculas y minúsculas
```bash
grep -i "palabra" archivo.txt
```

### Buscar recursivamente en un directorio
```bash
grep -r "palabra" /ruta/al/directorio
```

### Mostrar el número de línea de las coincidencias
```bash
grep -n "palabra" archivo.txt
```

### Listar archivos que contienen un patrón
```bash
grep -l "palabra" *.txt
```

## Tips
- Utiliza `grep` junto con otros comandos mediante tuberías (`|`) para filtrar resultados de manera efectiva.
- Combina `grep` con expresiones regulares para realizar búsquedas más complejas.
- Si buscas múltiples patrones, considera usar `grep -E` para habilitar expresiones regulares extendidas.