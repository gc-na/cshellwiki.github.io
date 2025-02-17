# [Linux] Bash cal <Uso equivalente en español>: Muestra un calendario

## Overview
El comando `cal` se utiliza para mostrar un calendario en la terminal. Permite visualizar el calendario de un mes específico o de un año completo, facilitando la consulta de fechas.

## Usage
La sintaxis básica del comando `cal` es la siguiente:

```
cal [opciones] [argumentos]
```

## Common Options
- `-m`: Muestra el calendario en un formato más compacto.
- `-y`: Muestra el calendario del año actual.
- `-3`: Muestra el mes actual, el anterior y el siguiente.
- `-j`: Muestra el calendario con los días del año (julianos).
- `-h`: Muestra el calendario en un formato horizontal.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `cal`:

1. Mostrar el calendario del mes actual:
   ```bash
   cal
   ```

2. Mostrar el calendario de un mes específico (por ejemplo, marzo de 2023):
   ```bash
   cal 03 2023
   ```

3. Mostrar el calendario del año actual:
   ```bash
   cal -y
   ```

4. Mostrar el calendario del mes actual, anterior y siguiente:
   ```bash
   cal -3
   ```

5. Mostrar el calendario con los días del año:
   ```bash
   cal -j
   ```

## Tips
- Puedes combinar opciones para personalizar la salida. Por ejemplo, `cal -m -3` mostrará un calendario compacto de tres meses.
- Si necesitas imprimir el calendario, considera redirigir la salida a un archivo usando `>` para guardarlo.
- Familiarízate con el uso de las opciones para aprovechar al máximo el comando `cal` y adaptarlo a tus necesidades.