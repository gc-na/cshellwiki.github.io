# [Linux] Bash udevadm uso: Gestión de dispositivos en el sistema

## Overview
El comando `udevadm` se utiliza para interactuar con el sistema de gestión de dispositivos `udev` en Linux. Permite a los administradores de sistemas observar y controlar la creación y eliminación de dispositivos en el sistema, así como gestionar las reglas de `udev`.

## Usage
La sintaxis básica del comando `udevadm` es la siguiente:

```bash
udevadm [opciones] [argumentos]
```

## Common Options
- `info`: Muestra información sobre un dispositivo específico.
- `trigger`: Dispara eventos `udev` para dispositivos.
- `settle`: Espera a que se completen todos los eventos `udev`.
- `control`: Permite habilitar o deshabilitar el servicio `udev`.
- `monitor`: Muestra eventos en tiempo real que ocurren en el sistema.

## Common Examples

### Mostrar información de un dispositivo
Para obtener información sobre un dispositivo específico, como `/dev/sda`, se puede usar:

```bash
udevadm info --query=all --name=/dev/sda
```

### Disparar eventos `udev`
Para forzar a `udev` a procesar eventos de dispositivos, se puede ejecutar:

```bash
udevadm trigger
```

### Esperar a que se completen los eventos
Para esperar a que todos los eventos de `udev` se completen, se utiliza:

```bash
udevadm settle
```

### Monitorear eventos en tiempo real
Para ver eventos de dispositivos en tiempo real, se puede usar:

```bash
udevadm monitor
```

### Controlar el servicio `udev`
Para deshabilitar temporalmente el servicio `udev`, se puede ejecutar:

```bash
udevadm control --stop
```

## Tips
- Asegúrate de tener privilegios de superusuario para ejecutar algunos comandos de `udevadm`.
- Utiliza `udevadm monitor` en una terminal separada para observar los cambios en tiempo real mientras realizas otras operaciones.
- Consulta la documentación oficial de `udev` para entender mejor cómo funcionan las reglas y eventos.