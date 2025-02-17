# [Linux] Bash ssh uso: Conectar a servidores de forma segura

## Overview
El comando `ssh` (Secure Shell) se utiliza para establecer una conexión segura con un servidor remoto. Permite a los usuarios acceder a la línea de comandos de otro sistema a través de una red, proporcionando autenticación y cifrado de datos.

## Usage
La sintaxis básica del comando `ssh` es la siguiente:

```
ssh [opciones] [usuario@]host
```

## Common Options
- `-p [puerto]`: Especifica el puerto a utilizar para la conexión SSH.
- `-i [archivo]`: Indica el archivo de clave privada a usar para la autenticación.
- `-v`: Muestra información detallada sobre el proceso de conexión, útil para depuración.
- `-X`: Habilita el reenvío de X11, permitiendo ejecutar aplicaciones gráficas de forma remota.
- `-C`: Activa la compresión de datos, lo que puede mejorar la velocidad de la conexión en redes lentas.

## Common Examples
1. **Conexión básica a un servidor:**
   ```bash
   ssh usuario@servidor.com
   ```

2. **Conexión a un servidor en un puerto diferente:**
   ```bash
   ssh -p 2222 usuario@servidor.com
   ```

3. **Uso de una clave privada específica:**
   ```bash
   ssh -i ~/.ssh/mi_clave_privada usuario@servidor.com
   ```

4. **Habilitar el reenvío de X11:**
   ```bash
   ssh -X usuario@servidor.com
   ```

5. **Conexión con compresión:**
   ```bash
   ssh -C usuario@servidor.com
   ```

## Tips
- Siempre utiliza claves SSH en lugar de contraseñas para mejorar la seguridad.
- Considera configurar el archivo `~/.ssh/config` para simplificar las conexiones a servidores frecuentes.
- Mantén tus claves privadas seguras y nunca las compartas.
- Usa la opción `-v` si experimentas problemas de conexión para obtener más información sobre el error.