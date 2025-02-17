# [Linux] Bash export uso equivalente: Establecer variables de entorno

## Overview
El comando `export` en Bash se utiliza para establecer variables de entorno que estarán disponibles para los procesos hijos del shell. Esto permite que las variables definidas en un shell se utilicen en otros programas o scripts que se ejecuten desde ese shell.

## Usage
La sintaxis básica del comando `export` es la siguiente:

```bash
export [opciones] [argumentos]
```

## Common Options
- `-n`: Elimina la exportación de una variable, haciendo que ya no esté disponible para los procesos hijos.
- `-p`: Muestra todas las variables de entorno que están actualmente exportadas.

## Common Examples

### Establecer una variable de entorno
Para establecer una variable de entorno llamada `MY_VAR` con el valor `Hello World`, puedes usar:

```bash
export MY_VAR="Hello World"
```

### Verificar una variable de entorno
Para verificar que la variable se ha establecido correctamente, puedes usar el comando `echo`:

```bash
echo $MY_VAR
```

### Exportar múltiples variables
Puedes exportar múltiples variables en una sola línea:

```bash
export VAR1="Valor1" VAR2="Valor2"
```

### Eliminar la exportación de una variable
Si deseas eliminar la exportación de `MY_VAR`, puedes hacerlo con:

```bash
export -n MY_VAR
```

### Listar todas las variables exportadas
Para ver todas las variables de entorno que has exportado, utiliza:

```bash
export -p
```

## Tips
- Siempre usa comillas alrededor de los valores que contienen espacios para evitar errores.
- Recuerda que las variables de entorno son sensibles a mayúsculas y minúsculas; `MY_VAR` y `my_var` son diferentes.
- Para hacer que las variables de entorno persistan entre sesiones, considera añadir el comando `export` en tu archivo de configuración de shell, como `~/.bashrc` o `~/.bash_profile`.