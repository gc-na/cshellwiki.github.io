# [Linux] Bash hwclock uso: Sincroniza el reloj del hardware

## Overview
El comando `hwclock` se utiliza para acceder y manipular el reloj de hardware del sistema. Este reloj es independiente del sistema operativo y se utiliza para mantener la hora cuando el sistema está apagado.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
hwclock [opciones] [argumentos]
```

## Common Options
- `--show`: Muestra la hora actual del reloj de hardware.
- `--set`: Establece la hora del reloj de hardware.
- `--hctosys`: Sincroniza la hora del sistema con la hora del reloj de hardware.
- `--systohc`: Sincroniza la hora del reloj de hardware con la hora del sistema.
- `--utc`: Indica que el reloj de hardware está configurado en UTC.

## Common Examples
1. **Mostrar la hora del reloj de hardware:**
   ```bash
   hwclock --show
   ```

2. **Sincronizar la hora del sistema con el reloj de hardware:**
   ```bash
   hwclock --hctosys
   ```

3. **Sincronizar el reloj de hardware con la hora del sistema:**
   ```bash
   hwclock --systohc
   ```

4. **Establecer una hora específica en el reloj de hardware:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

5. **Mostrar la hora en formato UTC:**
   ```bash
   hwclock --show --utc
   ```

## Tips
- Asegúrate de tener privilegios de superusuario al usar `hwclock`, especialmente para establecer la hora.
- Es recomendable sincronizar el reloj de hardware con la hora del sistema después de realizar cambios en la configuración de la hora.
- Utiliza la opción `--utc` si tu sistema utiliza UTC para evitar confusiones con las zonas horarias.