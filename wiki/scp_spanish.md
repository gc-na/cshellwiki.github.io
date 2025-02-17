# [Linux] Bash scp uso: Copiar archivos de forma segura entre hosts

## Overview
El comando `scp` (Secure Copy Protocol) se utiliza para copiar archivos y directorios de manera segura entre diferentes sistemas a través de una red. Utiliza el protocolo SSH para garantizar que la transferencia de datos sea segura y encriptada.

## Usage
La sintaxis básica del comando `scp` es la siguiente:

```bash
scp [opciones] [origen] [destino]
```

## Common Options
- `-r`: Copia directorios de forma recursiva.
- `-P`: Especifica el puerto a utilizar en el destino (ten en cuenta que es una P mayúscula).
- `-i`: Especifica el archivo de clave privada para la autenticación.
- `-v`: Muestra información detallada sobre el proceso de copia (modo verbose).
- `-C`: Habilita la compresión durante la transferencia.

## Common Examples
1. **Copiar un archivo local a un servidor remoto:**
   ```bash
   scp archivo.txt usuario@servidor:/ruta/destino/
   ```

2. **Copiar un archivo desde un servidor remoto a la máquina local:**
   ```bash
   scp usuario@servidor:/ruta/origen/archivo.txt /ruta/local/
   ```

3. **Copiar un directorio completo a un servidor remoto:**
   ```bash
   scp -r /ruta/local/directorio usuario@servidor:/ruta/destino/
   ```

4. **Copiar un archivo a un puerto específico:**
   ```bash
   scp -P 2222 archivo.txt usuario@servidor:/ruta/destino/
   ```

5. **Usar una clave privada para la autenticación:**
   ```bash
   scp -i /ruta/a/clave_privada archivo.txt usuario@servidor:/ruta/destino/
   ```

## Tips
- Asegúrate de tener los permisos adecuados en el servidor remoto para evitar errores de acceso.
- Utiliza la opción `-v` para depurar problemas de conexión o transferencia.
- Si transfieres archivos grandes, considera usar la opción `-C` para acelerar la transferencia mediante compresión.
- Siempre verifica la integridad de los archivos copiados, especialmente si son críticos para tu trabajo.