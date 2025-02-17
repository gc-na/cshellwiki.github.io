# [Linux] Bash screen uso: Manejo de sesiones de terminal

## Overview
El comando `screen` es una herramienta poderosa que permite a los usuarios gestionar múltiples sesiones de terminal en una sola ventana. Es especialmente útil para mantener procesos en ejecución incluso cuando se desconecta de la sesión, lo que lo convierte en una opción popular para administradores de sistemas y desarrolladores.

## Usage
La sintaxis básica del comando `screen` es la siguiente:

```bash
screen [opciones] [argumentos]
```

## Common Options
- `-S [nombre]`: Inicia una nueva sesión de screen con el nombre especificado.
- `-d -r`: Desconecta una sesión de screen y la vuelve a adjuntar.
- `-list`: Muestra una lista de todas las sesiones de screen activas.
- `-X [comando]`: Envía un comando a una sesión de screen específica.

## Common Examples
1. **Iniciar una nueva sesión de screen:**
   ```bash
   screen
   ```

2. **Iniciar una sesión con un nombre específico:**
   ```bash
   screen -S mi_sesion
   ```

3. **Desconectar de una sesión y volver a adjuntarla:**
   ```bash
   screen -d -r
   ```

4. **Listar todas las sesiones de screen activas:**
   ```bash
   screen -list
   ```

5. **Enviar un comando a una sesión específica:**
   ```bash
   screen -S mi_sesion -X quit
   ```

## Tips
- Utiliza nombres descriptivos para tus sesiones con `-S` para facilitar la identificación.
- Puedes dividir la pantalla en múltiples ventanas usando `Ctrl-a` seguido de `S` para dividir horizontalmente y `Ctrl-a` seguido de `|` para dividir verticalmente.
- Recuerda que puedes desconectar de una sesión presionando `Ctrl-a` seguido de `d`, lo que te permitirá volver a la terminal principal sin cerrar la sesión.