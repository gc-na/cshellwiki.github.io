# [Linux] Bash fc Uso equivalente: Editar y ejecutar comandos anteriores

## Overview
El comando `fc` en Bash se utiliza para listar, editar y ejecutar comandos anteriores en el historial de la terminal. Es una herramienta útil para corregir errores o repetir comandos sin tener que volver a escribirlos.

## Usage
La sintaxis básica del comando `fc` es la siguiente:

```bash
fc [opciones] [argumentos]
```

## Common Options
- `-l`: Lista los comandos en el historial.
- `-s`: Ejecuta el comando especificado sin abrir un editor.
- `-n`: No muestra los números de línea al listar los comandos.
- `-e`: Especifica un editor diferente para editar el comando.

## Common Examples

### Listar comandos en el historial
Para listar los últimos 10 comandos ejecutados:

```bash
fc -l -n -10
```

### Editar un comando específico
Si deseas editar el comando número 25 en el historial:

```bash
fc 25
```

### Ejecutar el último comando
Para ejecutar el último comando sin editarlo:

```bash
fc -s
```

### Usar un editor específico
Para editar el último comando usando `nano` como editor:

```bash
fc -e nano
```

## Tips
- Utiliza `fc -l` para revisar rápidamente los comandos que has ejecutado recientemente.
- Puedes combinar `fc` con otros comandos para mejorar tu flujo de trabajo, como redirigir la salida de un comando a un archivo.
- Recuerda que `fc` solo funciona con el historial de la sesión actual, así que asegúrate de que los comandos que deseas editar estén disponibles en el historial.