# [Linux] Bash trap uso: Captura señales y limpia recursos

## Overview
El comando `trap` en Bash se utiliza para capturar señales y ejecutar comandos específicos cuando se reciben estas señales. Esto es especialmente útil para limpiar recursos o realizar tareas de cierre antes de que un script termine su ejecución.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
trap [comando] [señal]
```

## Common Options
- `SIGINT`: Captura la señal de interrupción (Ctrl+C).
- `SIGTERM`: Captura la señal de terminación.
- `EXIT`: Ejecuta un comando cuando el script termina, ya sea de forma normal o por una señal.

## Common Examples

### Ejemplo 1: Capturar SIGINT
Este ejemplo muestra cómo capturar la señal de interrupción y ejecutar un comando específico.

```bash
trap 'echo "Interrupción recibida. Saliendo..."; exit' SIGINT
while true; do
    echo "Ejecutando..."
    sleep 1
done
```

### Ejemplo 2: Limpiar recursos al salir
Aquí se utiliza `trap` para limpiar un archivo temporal al salir del script.

```bash
trap 'rm -f /tmp/mi_archivo.tmp' EXIT
echo "Creando archivo temporal..."
touch /tmp/mi_archivo.tmp
# Aquí se pueden realizar otras operaciones
```

### Ejemplo 3: Capturar múltiples señales
Este ejemplo muestra cómo capturar múltiples señales y ejecutar diferentes comandos.

```bash
trap 'echo "Saliendo por SIGINT"; exit' SIGINT
trap 'echo "Saliendo por SIGTERM"; exit' SIGTERM
while true; do
    echo "Esperando señales..."
    sleep 2
done
```

## Tips
- Siempre es una buena práctica limpiar recursos al finalizar un script, especialmente si se crean archivos temporales o se abren conexiones.
- Puedes usar `trap` para manejar errores y asegurarte de que ciertas acciones se realicen incluso si el script se interrumpe inesperadamente.
- Recuerda que `trap` puede ser utilizado para depurar scripts, permitiéndote saber cuándo y por qué un script se detiene.