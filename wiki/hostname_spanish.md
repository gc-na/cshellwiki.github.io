# [Linux] Bash hostname uso: [mostrar o establecer el nombre del host]

## Overview
El comando `hostname` se utiliza en sistemas operativos basados en Unix para mostrar o establecer el nombre del host del sistema. El nombre del host es la identificación única de una máquina en una red.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
hostname [opciones] [argumentos]
```

## Common Options
- `-a`, `--alias`: Muestra el alias del host.
- `-d`, `--domain`: Muestra el nombre de dominio del host.
- `-f`, `--fqdn`: Muestra el nombre de dominio completamente calificado.
- `-i`, `--ip-address`: Muestra la dirección IP del host.
- `-s`, `--short`: Muestra solo el nombre corto del host.
- `--help`: Muestra la ayuda sobre el uso del comando.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `hostname`:

1. **Mostrar el nombre del host actual:**
   ```bash
   hostname
   ```

2. **Mostrar el nombre de dominio completamente calificado:**
   ```bash
   hostname -f
   ```

3. **Mostrar la dirección IP del host:**
   ```bash
   hostname -i
   ```

4. **Establecer un nuevo nombre de host:**
   ```bash
   sudo hostname nuevo-nombre
   ```

5. **Mostrar el nombre corto del host:**
   ```bash
   hostname -s
   ```

## Tips
- Asegúrate de tener privilegios de superusuario al cambiar el nombre del host, ya que se requiere permisos especiales.
- Después de cambiar el nombre del host, es recomendable reiniciar el sistema o reiniciar los servicios de red para que los cambios surtan efecto.
- Puedes verificar el cambio del nombre del host utilizando el comando `hostname` nuevamente después de realizar la modificación.