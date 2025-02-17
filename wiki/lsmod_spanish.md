# [Linux] Bash lsmod Uso: Muestra los módulos del kernel cargados

## Overview
El comando `lsmod` se utiliza en sistemas Linux para mostrar una lista de los módulos del kernel que están actualmente cargados en la memoria. Es una herramienta útil para los administradores del sistema que necesitan verificar qué controladores y módulos están activos en su sistema.

## Usage
La sintaxis básica del comando `lsmod` es la siguiente:

```bash
lsmod [opciones]
```

## Common Options
El comando `lsmod` no tiene muchas opciones, pero aquí están algunas de las más comunes:

- **(sin opciones)**: Muestra la lista de módulos cargados.
- **-h, --help**: Muestra la ayuda y la información sobre el uso del comando.

## Common Examples

### Ejemplo 1: Listar módulos cargados
Para ver todos los módulos del kernel que están actualmente cargados, simplemente ejecuta:

```bash
lsmod
```

### Ejemplo 2: Filtrar la salida
Si deseas buscar un módulo específico, puedes combinar `lsmod` con `grep`. Por ejemplo, para buscar el módulo `nvidia`:

```bash
lsmod | grep nvidia
```

### Ejemplo 3: Ver módulos con detalles
Aunque `lsmod` no proporciona detalles extensos, puedes usar `modinfo` para obtener más información sobre un módulo específico. Primero, usa `lsmod` para encontrar el módulo y luego:

```bash
modinfo nvidia
```

## Tips
- Utiliza `lsmod` junto con otros comandos como `modprobe` y `rmmod` para gestionar módulos del kernel de manera efectiva.
- Recuerda que los módulos cargados pueden afectar el rendimiento del sistema, así que verifica regularmente los módulos que están activos.
- Si experimentas problemas con hardware, revisa `lsmod` para asegurarte de que los módulos necesarios están cargados.