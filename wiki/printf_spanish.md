# [Linux] Bash printf Uso: Formatear y mostrar texto

## Overview
El comando `printf` en Bash se utiliza para formatear y mostrar texto en la salida estándar. A diferencia de `echo`, `printf` permite un control más preciso sobre el formato de la salida, lo que lo hace ideal para crear mensajes bien estructurados.

## Usage
La sintaxis básica del comando `printf` es la siguiente:

```bash
printf [opciones] [formato] [argumentos]
```

## Common Options
- `-v`: Asigna el resultado a una variable en lugar de imprimirlo.
- `-f`: Especifica un formato de salida.
- `--help`: Muestra la ayuda sobre el comando y sus opciones.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `printf`:

### Ejemplo 1: Imprimir texto simple
```bash
printf "Hola, mundo!\n"
```

### Ejemplo 2: Formatear números
```bash
printf "El número es: %.2f\n" 3.14159
```

### Ejemplo 3: Imprimir múltiples líneas
```bash
printf "Nombre: %s\nEdad: %d\n" "Juan" 30
```

### Ejemplo 4: Asignar a una variable
```bash
resultado=$(printf "Resultado: %.1f\n" 12.345)
echo $resultado
```

## Tips
- Utiliza `\n` para agregar saltos de línea en la salida.
- Aprovecha los especificadores de formato como `%s` para cadenas y `%d` para enteros para un mejor control de la salida.
- Recuerda que `printf` no añade automáticamente un salto de línea al final, a diferencia de `echo`.