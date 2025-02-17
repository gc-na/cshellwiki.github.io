# [Linux] Bash nohup uso equivalente: Ejecutar procesos que persisten después de cerrar la sesión

## Overview
El comando `nohup` (no hang up) se utiliza en sistemas Unix y Linux para ejecutar procesos que deben continuar funcionando incluso después de que el usuario haya cerrado la sesión o la terminal. Es especialmente útil para ejecutar tareas de larga duración sin preocuparse por la desconexión.

## Usage
La sintaxis básica del comando `nohup` es la siguiente:

```bash
nohup [opciones] [comando] [argumentos] &
```

El símbolo `&` al final se utiliza para ejecutar el comando en segundo plano.

## Common Options
- `-h`, `--help`: Muestra la ayuda sobre el uso del comando.
- `-v`, `--version`: Muestra la versión del comando `nohup`.
- `-o archivo`: Redirige la salida estándar a un archivo específico.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `nohup`:

1. **Ejecutar un script en segundo plano:**
   ```bash
   nohup ./mi_script.sh &
   ```

2. **Ejecutar un comando y redirigir la salida a un archivo:**
   ```bash
   nohup ping google.com > salida_ping.txt &
   ```

3. **Ejecutar un proceso de larga duración:**
   ```bash
   nohup python mi_programa.py &
   ```

4. **Ejecutar un comando con salida de error redirigida:**
   ```bash
   nohup ./mi_programa.sh > salida.txt 2> errores.txt &
   ```

## Tips
- Siempre redirige la salida de tus comandos a un archivo para poder revisar los resultados más tarde.
- Usa `jobs` para ver los procesos en segundo plano y `fg` para llevar uno de ellos de vuelta al primer plano si es necesario.
- Recuerda que los procesos ejecutados con `nohup` seguirán funcionando incluso si cierras la terminal, así que asegúrate de que no consuman recursos innecesarios.