# [Linux] Bash df Uso: Muestra el espacio en disco disponible

## Overview
El comando `df` en Bash se utiliza para mostrar información sobre el espacio en disco disponible en los sistemas de archivos montados. Proporciona detalles sobre la cantidad total de espacio, el espacio utilizado y el espacio libre en cada sistema de archivos.

## Usage
La sintaxis básica del comando `df` es la siguiente:

```bash
df [opciones] [argumentos]
```

## Common Options
- `-h`: Muestra los tamaños en un formato legible para humanos (por ejemplo, en KB, MB, GB).
- `-T`: Muestra el tipo de sistema de archivos.
- `-a`: Muestra todos los sistemas de archivos, incluyendo aquellos que tienen 0 bloques.
- `-i`: Muestra información sobre inodos en lugar de bloques.

## Common Examples
- Para ver el espacio en disco de todos los sistemas de archivos en un formato legible para humanos:

```bash
df -h
```

- Para mostrar el tipo de sistema de archivos junto con la información del espacio:

```bash
df -T
```

- Para incluir todos los sistemas de archivos, incluso los que no están en uso:

```bash
df -a
```

- Para ver la información de inodos:

```bash
df -i
```

## Tips
- Utiliza la opción `-h` para facilitar la lectura de los resultados, especialmente en sistemas con grandes volúmenes de datos.
- Combina opciones, por ejemplo, `df -hT` para obtener un resumen más completo.
- Revisa regularmente el espacio en disco para evitar problemas de almacenamiento en el sistema.