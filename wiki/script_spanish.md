# [Linux] Bash script uso: Grabar sesiones de terminal

## Overview
El comando `script` se utiliza para grabar una sesión de terminal en un archivo. Esto es útil para registrar la salida de comandos y la interacción con el sistema, permitiendo revisitar la sesión más tarde.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
script [opciones] [archivo]
```

## Common Options
- `-a`: Añadir la salida al final del archivo existente en lugar de sobrescribirlo.
- `-c`: Ejecutar un comando específico y grabar su salida.
- `-f`: Forzar la salida en tiempo real, mostrando los datos a medida que se generan.
- `-q`: Modo silencioso, no muestra mensajes de inicio y final.

## Common Examples

1. **Grabar una sesión en un archivo llamado `mi_sesion.txt`:**

   ```bash
   script mi_sesion.txt
   ```

2. **Grabar una sesión y añadirla a un archivo existente:**

   ```bash
   script -a mi_sesion.txt
   ```

3. **Ejecutar un comando específico y grabar su salida:**

   ```bash
   script -c "ls -l" salida.txt
   ```

4. **Grabar una sesión en tiempo real:**

   ```bash
   script -f mi_sesion.txt
   ```

5. **Iniciar una sesión en modo silencioso:**

   ```bash
   script -q mi_sesion.txt
   ```

## Tips
- Asegúrate de finalizar la sesión correctamente usando el comando `exit` para que el archivo se cierre adecuadamente.
- Utiliza la opción `-a` si deseas mantener un registro continuo de varias sesiones en el mismo archivo.
- Revisa el archivo grabado con un editor de texto o utilizando comandos como `cat` o `less` para visualizar el contenido.