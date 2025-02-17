# [Linux] Bash awk Uso: Procesamiento de texto y análisis de datos

## Overview
El comando `awk` es una herramienta poderosa en Bash que se utiliza para el procesamiento de texto y el análisis de datos. Permite manipular y extraer información de archivos de texto, facilitando tareas como la búsqueda, la modificación y la generación de informes.

## Usage
La sintaxis básica del comando `awk` es la siguiente:

```bash
awk [opciones] [argumentos]
```

## Common Options
- `-F`: Especifica el delimitador de campo. Por defecto, `awk` utiliza espacios en blanco.
- `-v`: Permite definir variables de entorno que se pueden usar dentro del script `awk`.
- `-f`: Indica que el siguiente argumento es un archivo que contiene un script `awk`.

## Common Examples

### Ejemplo 1: Imprimir la primera columna de un archivo
```bash
awk '{print $1}' archivo.txt
```
Este comando imprime la primera columna de cada línea en `archivo.txt`.

### Ejemplo 2: Usar un delimitador personalizado
```bash
awk -F, '{print $2}' archivo.csv
```
Aquí, `awk` utiliza la coma como delimitador y muestra la segunda columna de un archivo CSV.

### Ejemplo 3: Filtrar líneas que cumplen una condición
```bash
awk '$3 > 50' archivo.txt
```
Este comando imprime las líneas donde el tercer campo es mayor que 50.

### Ejemplo 4: Contar el número de líneas en un archivo
```bash
awk 'END {print NR}' archivo.txt
```
Este comando cuenta y muestra el número total de líneas en `archivo.txt`.

### Ejemplo 5: Sumar valores de una columna
```bash
awk '{sum += $2} END {print sum}' archivo.txt
```
Aquí, `awk` suma todos los valores de la segunda columna y muestra el resultado al final.

## Tips
- Siempre verifica el delimitador de tus archivos. Usa `-F` para especificar el correcto si no es un espacio.
- Puedes combinar `awk` con otros comandos de Unix, como `grep` y `sort`, para realizar análisis más complejos.
- Practica con archivos pequeños antes de aplicar `awk` a conjuntos de datos más grandes para familiarizarte con su sintaxis y comportamiento.