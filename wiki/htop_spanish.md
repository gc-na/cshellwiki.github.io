# [Linux] Bash htop Uso: Monitorización interactiva de procesos

## Overview
El comando `htop` es una herramienta de monitorización interactiva que permite visualizar en tiempo real los procesos que se están ejecutando en un sistema Linux. A diferencia de `top`, `htop` ofrece una interfaz más amigable y permite la navegación y gestión de procesos de manera más sencilla.

## Usage
La sintaxis básica del comando `htop` es la siguiente:

```bash
htop [opciones] [argumentos]
```

## Common Options
- `-h`, `--help`: Muestra la ayuda y las opciones disponibles.
- `-s`, `--sort`: Permite ordenar los procesos por diferentes criterios (por ejemplo, uso de CPU o memoria).
- `-p`, `--pid`: Muestra solo los procesos con los identificadores de proceso (PID) especificados.
- `-u`, `--user`: Filtra los procesos para mostrar solo aquellos pertenecientes a un usuario específico.

## Common Examples
- Para iniciar `htop` simplemente, ejecuta:

```bash
htop
```

- Para ordenar los procesos por uso de CPU:

```bash
htop -s PERCENT_CPU
```

- Para mostrar solo los procesos de un usuario específico, por ejemplo, "usuario1":

```bash
htop -u usuario1
```

- Para mostrar información de procesos específicos por PID, por ejemplo, 1234:

```bash
htop -p 1234
```

## Tips
- Usa las teclas de función (F1 a F10) para acceder a diferentes funciones dentro de `htop`, como la ayuda (F1) o la búsqueda (F3).
- Puedes matar un proceso seleccionándolo y presionando `F9`, lo que te permitirá finalizar procesos de manera rápida.
- Personaliza la visualización de columnas y la información que deseas ver presionando `F2` para acceder a la configuración.