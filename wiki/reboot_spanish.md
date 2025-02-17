# [Linux] Bash reboot uso: Reiniciar el sistema

El comando `reboot` se utiliza para reiniciar el sistema operativo de manera controlada.

## Overview
El comando `reboot` permite reiniciar el sistema de forma inmediata. Este comando es útil cuando se requieren aplicar cambios en la configuración del sistema o después de instalar actualizaciones importantes.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
reboot [opciones] [argumentos]
```

## Common Options
- `-f`: Fuerza el reinicio sin realizar un apagado limpio.
- `-p`: Apaga el sistema después de reiniciar.
- `-h`: Detiene el sistema sin reiniciarlo.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `reboot`:

1. **Reiniciar el sistema de forma normal:**
   ```bash
   reboot
   ```

2. **Reiniciar el sistema forzadamente:**
   ```bash
   reboot -f
   ```

3. **Reiniciar y apagar el sistema:**
   ```bash
   reboot -p
   ```

4. **Reiniciar el sistema con un mensaje personalizado:**
   ```bash
   shutdown -r now "El sistema se reiniciará en breve."
   ```

## Tips
- Asegúrate de guardar todos tus trabajos antes de ejecutar el comando `reboot`, ya que se cerrarán todas las aplicaciones abiertas.
- Utiliza el comando `shutdown` si deseas programar un reinicio en lugar de hacerlo de inmediato.
- Si estás en un entorno de producción, considera notificar a los usuarios sobre el reinicio programado para evitar pérdida de datos.