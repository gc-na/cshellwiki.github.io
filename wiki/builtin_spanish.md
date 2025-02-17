# [Linux] Bash builtin comando `builtin`: Ejecutar comandos internos

## Overview
El comando `builtin` en Bash se utiliza para ejecutar comandos internos de la shell, permitiendo que se omitan los comandos externos que podrían tener el mismo nombre. Esto es útil para asegurarse de que se está utilizando la versión interna de un comando, especialmente en situaciones donde hay conflictos de nombres.

## Usage
La sintaxis básica del comando `builtin` es la siguiente:

```bash
builtin [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas opciones comunes que se pueden utilizar con el comando `builtin`:

- `-p`: Muestra la versión interna del comando sin ejecutar.
- `-f`: Evita que se busquen funciones con el mismo nombre que el comando.

## Common Examples

### Ejecutar un comando interno
Para asegurarte de que estás ejecutando la versión interna de `echo`, puedes usar:

```bash
builtin echo "Este es un mensaje desde el comando interno."
```

### Verificar la versión interna de un comando
Si deseas verificar qué versión interna de un comando se utilizará, puedes usar la opción `-p`:

```bash
builtin -p echo
```

### Evitar funciones con el mismo nombre
Si tienes una función llamada `cd` y quieres asegurarte de que se ejecute el comando interno `cd`, puedes usar:

```bash
builtin cd /ruta/deseada
```

## Tips
- Utiliza `builtin` cuando necesites asegurarte de que estás utilizando la versión interna de un comando, especialmente si has definido funciones con el mismo nombre.
- Es útil para depurar problemas en scripts donde el comportamiento de un comando puede verse afectado por funciones personalizadas.
- Recuerda que no todos los comandos tienen una versión interna; verifica la documentación si no estás seguro.