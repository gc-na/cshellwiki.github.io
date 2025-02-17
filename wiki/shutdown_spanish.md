# [Linux] Bash shutdown uso: Apagar o reiniciar el sistema

El comando `shutdown` se utiliza para apagar o reiniciar un sistema Linux de manera segura.

## Overview
El comando `shutdown` permite a los usuarios y administradores de sistemas apagar o reiniciar el sistema de forma controlada. Esto es útil para realizar tareas de mantenimiento, actualizaciones o simplemente para apagar el sistema de manera segura.

## Usage
La sintaxis básica del comando es la siguiente:

```
shutdown [opciones] [tiempo] [mensaje]
```

## Common Options
- `-h` o `--halt`: Apaga el sistema.
- `-r` o `--reboot`: Reinicia el sistema.
- `-P` o `--poweroff`: Apaga el sistema y lo apaga completamente.
- `now`: Indica que la acción debe realizarse de inmediato.
- `+m`: Indica que la acción se debe realizar después de `m` minutos.
- `hh:mm`: Especifica una hora exacta para realizar la acción.

## Common Examples
1. **Apagar el sistema inmediatamente:**
   ```bash
   shutdown now
   ```

2. **Reiniciar el sistema en 5 minutos:**
   ```bash
   shutdown -r +5
   ```

3. **Apagar el sistema a las 10:30 PM:**
   ```bash
   shutdown 22:30
   ```

4. **Enviar un mensaje a los usuarios antes de apagar:**
   ```bash
   shutdown -h now "El sistema se apagará en 1 minuto. Guarde su trabajo."
   ```

5. **Reiniciar el sistema de forma inmediata:**
   ```bash
   shutdown -r now
   ```

## Tips
- Siempre notifique a los usuarios antes de apagar o reiniciar el sistema para evitar la pérdida de datos.
- Utiliza la opción `-h` si deseas asegurarte de que el sistema se apague completamente.
- Puedes cancelar un apagado programado usando el comando `shutdown -c`.