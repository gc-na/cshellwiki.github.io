# [Linux] Bash readonly uso equivalente: Establecer variables como de solo lectura

## Overview
El comando `readonly` en Bash se utiliza para marcar variables como de solo lectura. Esto significa que una vez que una variable ha sido declarada como `readonly`, su valor no puede ser modificado ni eliminada durante la sesión actual del shell.

## Usage
La sintaxis básica del comando `readonly` es la siguiente:

```bash
readonly [nombre_variable]
```

## Common Options
El comando `readonly` no tiene muchas opciones, pero aquí hay algunas que son útiles:

- `-p`: Muestra todas las variables que están marcadas como de solo lectura.

## Common Examples

### Ejemplo 1: Declarar una variable como de solo lectura
```bash
readonly MI_VARIABLE="Hola Mundo"
```
En este ejemplo, `MI_VARIABLE` se establece como una variable de solo lectura con el valor "Hola Mundo".

### Ejemplo 2: Intentar modificar una variable de solo lectura
```bash
readonly MI_VARIABLE="Hola Mundo"
MI_VARIABLE="Nuevo Valor"  # Esto generará un error
```
Aquí, intentar cambiar el valor de `MI_VARIABLE` resultará en un error porque ya está marcada como de solo lectura.

### Ejemplo 3: Mostrar variables de solo lectura
```bash
readonly -p
```
Este comando mostrará todas las variables que han sido declaradas como de solo lectura en la sesión actual.

## Tips
- Utiliza `readonly` para proteger variables importantes que no deberían ser modificadas accidentalmente.
- Recuerda que las variables de solo lectura son útiles en scripts donde la integridad de los datos es crucial.
- Puedes usar `declare -r` como una alternativa para declarar variables de solo lectura, lo que puede ser más claro en algunos contextos.