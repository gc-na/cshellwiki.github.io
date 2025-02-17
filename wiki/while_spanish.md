# [Linux] Bash while uso: Ejecutar comandos repetidamente

## Overview
El comando `while` en Bash se utiliza para ejecutar un bloque de comandos de manera repetitiva mientras una condición especificada sea verdadera. Es una herramienta poderosa para automatizar tareas que requieren repetición hasta que se cumpla una condición.

## Usage
La sintaxis básica del comando `while` es la siguiente:

```bash
while [ condición ]; do
    # comandos a ejecutar
done
```

## Common Options
El comando `while` no tiene opciones específicas, pero la condición puede incluir diversas expresiones y comandos que devuelvan un estado de éxito o fracaso. Algunas de las condiciones comunes son:

- `true`: siempre devuelve verdadero, ejecutando el bucle indefinidamente.
- `false`: siempre devuelve falso, evitando que se ejecute el bucle.
- Comparaciones numéricas: como `-eq`, `-ne`, `-lt`, `-le`, `-gt`, `-ge`.
- Comprobaciones de archivos: como `-e` (existe), `-d` (es un directorio), `-f` (es un archivo regular).

## Common Examples

### Ejemplo 1: Contador simple
Este ejemplo muestra cómo contar del 1 al 5.

```bash
contador=1
while [ $contador -le 5 ]; do
    echo "Contador: $contador"
    contador=$((contador + 1))
done
```

### Ejemplo 2: Leer líneas de un archivo
Este ejemplo lee un archivo línea por línea.

```bash
archivo="mi_archivo.txt"
while IFS= read -r linea; do
    echo "Línea: $linea"
done < "$archivo"
```

### Ejemplo 3: Bucle infinito
Este ejemplo ejecuta un bucle infinito que se puede detener con `Ctrl+C`.

```bash
while true; do
    echo "Este bucle se ejecuta indefinidamente."
    sleep 1
done
```

## Tips
- Asegúrate de que la condición del bucle eventualmente se vuelva falsa para evitar bucles infinitos no deseados.
- Usa `sleep` dentro del bucle para evitar que consuma demasiados recursos del sistema en bucles que se ejecutan rápidamente.
- Considera el uso de `break` para salir del bucle bajo ciertas condiciones y `continue` para saltar a la siguiente iteración.