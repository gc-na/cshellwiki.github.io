# [Linux] Bash wall uso: Enviar mensajes a todos los usuarios conectados

## Overview
El comando `wall` (write all) se utiliza en sistemas Unix y Linux para enviar un mensaje a todos los usuarios conectados al sistema. Este comando es útil para notificar a los usuarios sobre eventos importantes, como el mantenimiento del sistema o la finalización de tareas.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
wall [opciones] [argumentos]
```

## Common Options
- `-n`: No enviar el mensaje a los usuarios que no están en la terminal.
- `-s`: Silenciar el mensaje, es decir, no mostrar el nombre del usuario que envía el mensaje.

## Common Examples

1. **Enviar un mensaje simple a todos los usuarios:**

   ```bash
   wall "El sistema se reiniciará en 10 minutos."
   ```

2. **Enviar un mensaje desde un archivo:**

   ```bash
   wall < mensaje.txt
   ```

3. **Enviar un mensaje con opción de silencio:**

   ```bash
   wall -s "Mantenimiento programado en 30 minutos."
   ```

4. **Enviar un mensaje sin notificar a usuarios desconectados:**

   ```bash
   wall -n "Por favor, guarden su trabajo."
   ```

## Tips
- Asegúrate de que el mensaje sea claro y conciso para que todos los usuarios lo entiendan rápidamente.
- Utiliza `wall` con moderación, ya que los mensajes pueden ser intrusivos si se envían con frecuencia.
- Considera el horario al enviar mensajes, para no interrumpir a los usuarios en momentos críticos.