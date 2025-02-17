# [Linux] Bash fsck uso: Comprobar y reparar sistemas de archivos

## Overview
El comando `fsck` (File System Consistency Check) se utiliza para verificar y reparar la integridad de los sistemas de archivos en Linux. Es una herramienta esencial para mantener la salud de los discos y prevenir la pérdida de datos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
fsck [opciones] [argumentos]
```

## Common Options
- `-a`: Intenta arreglar automáticamente los problemas encontrados.
- `-n`: Realiza una verificación sin hacer cambios, útil para revisar el estado del sistema de archivos.
- `-y`: Responde "sí" a todas las preguntas, permitiendo que `fsck` realice correcciones automáticamente.
- `-t`: Especifica el tipo de sistema de archivos a verificar (por ejemplo, ext4, xfs).

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `fsck`:

1. **Verificar un sistema de archivos específico:**
   ```bash
   fsck /dev/sda1
   ```

2. **Verificar y reparar automáticamente:**
   ```bash
   fsck -a /dev/sda1
   ```

3. **Realizar una verificación sin cambios:**
   ```bash
   fsck -n /dev/sda1
   ```

4. **Forzar la verificación de un sistema de archivos:**
   ```bash
   fsck -f /dev/sda1
   ```

5. **Verificar todos los sistemas de archivos en /etc/fstab:**
   ```bash
   fsck -A
   ```

## Tips
- Siempre es recomendable hacer una copia de seguridad de los datos importantes antes de ejecutar `fsck`, especialmente si se va a utilizar con opciones que modifican el sistema de archivos.
- Ejecuta `fsck` en modo de usuario único o desde un entorno de recuperación para evitar conflictos con procesos que utilizan el sistema de archivos.
- Utiliza la opción `-n` para realizar una verificación inicial sin realizar cambios, lo que te permitirá evaluar el estado del sistema de archivos antes de aplicar correcciones.