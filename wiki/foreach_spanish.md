# [Linux] Bash foreach uso equivalente: Ejecutar comandos en una lista

## Overview
El comando `foreach` en Bash se utiliza para iterar sobre una lista de elementos y ejecutar un conjunto de comandos para cada uno de ellos. Es útil para realizar operaciones repetitivas de manera eficiente.

## Usage
La sintaxis básica del comando `foreach` es la siguiente:

```bash
foreach variable (lista)
    comando
end
```

## Common Options
El comando `foreach` en sí no tiene muchas opciones, ya que es más un constructo de control de flujo. Sin embargo, se pueden utilizar opciones en los comandos que se ejecutan dentro del bucle. 

## Common Examples

### Ejemplo 1: Iterar sobre una lista de archivos
```bash
foreach archivo (file1.txt file2.txt file3.txt)
    echo "Procesando $archivo"
end
```

### Ejemplo 2: Ejecutar un comando en múltiples directorios
```bash
foreach dir (dir1 dir2 dir3)
    cd $dir
    ls
end
```

### Ejemplo 3: Realizar operaciones matemáticas
```bash
foreach num (1 2 3 4 5)
    echo "El cuadrado de $num es $(($num * $num))"
end
```

## Tips
- Asegúrate de que la lista de elementos esté correctamente definida para evitar errores.
- Utiliza comillas si los elementos de la lista contienen espacios.
- Considera el uso de `for` en lugar de `foreach` si estás trabajando en un script Bash, ya que `foreach` no es un comando nativo de Bash, sino de tcsh. En Bash, el bucle `for` es más comúnmente utilizado.