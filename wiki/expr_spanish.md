# [Linux] Bash expr Uso equivalente: Evaluar expresiones y realizar cálculos

## Overview
El comando `expr` se utiliza en Bash para evaluar expresiones y realizar cálculos aritméticos, así como para manipular cadenas de texto. Es una herramienta útil para realizar operaciones simples directamente desde la línea de comandos.

## Usage
La sintaxis básica del comando `expr` es la siguiente:

```bash
expr [opciones] [argumentos]
```

## Common Options
- `-e`: Permite evaluar expresiones.
- `length`: Devuelve la longitud de una cadena.
- `index`: Devuelve la posición de la primera aparición de un carácter en una cadena.
- `substr`: Extrae una subcadena de una cadena dada.

## Common Examples

### Ejemplo 1: Sumar dos números
```bash
expr 5 + 3
```
Este comando devuelve `8`, que es la suma de 5 y 3.

### Ejemplo 2: Calcular la longitud de una cadena
```bash
expr length "Hola Mundo"
```
Este comando devuelve `10`, que es la longitud de la cadena "Hola Mundo".

### Ejemplo 3: Encontrar la posición de un carácter
```bash
expr index "Hola Mundo" "M"
```
Este comando devuelve `6`, que es la posición de la letra "M" en la cadena.

### Ejemplo 4: Extraer una subcadena
```bash
expr substr "Hola Mundo" 1 4
```
Este comando devuelve `Hola`, que es la subcadena extraída desde la posición 1 y con una longitud de 4.

## Tips
- Recuerda que `expr` requiere espacios alrededor de los operadores, de lo contrario, no funcionará correctamente.
- Para operaciones más complejas, considera usar `$(( ))` para la aritmética, ya que es más potente y flexible.
- `expr` es útil en scripts de shell, pero para tareas más avanzadas, evalúa el uso de lenguajes de programación como Python o Perl.