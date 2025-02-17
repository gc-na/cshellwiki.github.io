# [Linux] Bash pwd uso equivalente: Muestra el directorio de trabajo actual

## Overview
El comando `pwd` (print working directory) se utiliza en Bash para mostrar la ruta completa del directorio de trabajo actual en el que te encuentras. Es una herramienta fundamental para navegar por el sistema de archivos y verificar tu ubicación.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
pwd [opciones]
```

## Common Options
- `-L`: Muestra la ruta lógica del directorio actual, que puede incluir enlaces simbólicos.
- `-P`: Muestra la ruta física del directorio actual, resolviendo todos los enlaces simbólicos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `pwd`:

1. **Mostrar el directorio actual:**

   ```bash
   pwd
   ```

2. **Mostrar la ruta lógica:**

   ```bash
   pwd -L
   ```

3. **Mostrar la ruta física:**

   ```bash
   pwd -P
   ```

## Tips
- Usa `pwd` regularmente para asegurarte de que estás en el directorio correcto antes de ejecutar otros comandos.
- Combina `pwd` con otros comandos como `cd` para verificar tu ubicación después de cambiar de directorio.
- Recuerda que `pwd` no requiere argumentos adicionales para funcionar, lo que lo hace rápido y fácil de usar.