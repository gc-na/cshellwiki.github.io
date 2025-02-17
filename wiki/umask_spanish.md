# [Linux] Bash umask Uso: Establecer permisos predeterminados para archivos y directorios

## Overview
El comando `umask` se utiliza en sistemas Unix y Linux para establecer los permisos predeterminados de los archivos y directorios que se crean en el sistema. Este comando define una máscara que determina qué permisos no se asignarán a los nuevos archivos y directorios.

## Usage
La sintaxis básica del comando `umask` es la siguiente:

```bash
umask [opciones] [máscara]
```

## Common Options
- `-S`: Muestra la máscara de permisos en formato simbólico.
- `-p`: Muestra la máscara de permisos actual en formato de octal.

## Common Examples
A continuación se presentan algunos ejemplos prácticos del uso del comando `umask`:

1. **Ver la máscara de permisos actual:**
   ```bash
   umask
   ```

2. **Establecer una nueva máscara de permisos:**
   ```bash
   umask 027
   ```
   Esto establece que los nuevos archivos tendrán permisos de lectura y escritura para el propietario, lectura para el grupo y sin permisos para otros.

3. **Mostrar la máscara en formato simbólico:**
   ```bash
   umask -S
   ```

4. **Restablecer la máscara a su valor predeterminado:**
   ```bash
   umask 0022
   ```

## Tips
- Es recomendable verificar la máscara de permisos actual antes de crear archivos o directorios importantes para asegurarte de que los permisos sean los deseados.
- Puedes agregar el comando `umask` en tu archivo de configuración de shell (como `.bashrc` o `.bash_profile`) para establecer una máscara predeterminada cada vez que inicies sesión.
- Recuerda que los permisos se establecen en formato octal, donde cada dígito representa permisos para el propietario, el grupo y otros, respectivamente.