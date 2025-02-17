# [Linux] Bash mysql uso: Interactuar con bases de datos MySQL

## Overview
El comando `mysql` es una herramienta de línea de comandos que permite a los usuarios interactuar con bases de datos MySQL. Con `mysql`, puedes ejecutar consultas SQL, gestionar bases de datos y realizar diversas operaciones de administración.

## Usage
La sintaxis básica del comando `mysql` es la siguiente:

```bash
mysql [opciones] [argumentos]
```

## Common Options
- `-u, --user=usuario`: Especifica el nombre de usuario para conectarse a la base de datos.
- `-p, --password`: Solicita la contraseña del usuario. Si se omite, se pedirá al usuario que la ingrese.
- `-h, --host=host`: Especifica el host donde se encuentra el servidor MySQL.
- `-D, --database=base_de_datos`: Selecciona la base de datos a utilizar al conectarse.
- `-e, --execute=consulta`: Permite ejecutar una consulta SQL directamente desde la línea de comandos.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `mysql`:

1. **Conectar a MySQL con un usuario y contraseña:**
   ```bash
   mysql -u usuario -p
   ```

2. **Conectar a una base de datos específica:**
   ```bash
   mysql -u usuario -p -D nombre_base_datos
   ```

3. **Ejecutar una consulta SQL directamente:**
   ```bash
   mysql -u usuario -p -e "SELECT * FROM tabla;"
   ```

4. **Importar un archivo SQL a una base de datos:**
   ```bash
   mysql -u usuario -p nombre_base_datos < archivo.sql
   ```

5. **Exportar una base de datos a un archivo SQL:**
   ```bash
   mysqldump -u usuario -p nombre_base_datos > archivo.sql
   ```

## Tips
- Siempre utiliza el flag `-p` para que la contraseña no se muestre en la línea de comandos.
- Si trabajas con múltiples bases de datos, considera usar el flag `-D` para evitar confusiones.
- Utiliza `mysqldump` para hacer copias de seguridad de tus bases de datos regularmente.
- Familiarízate con las consultas SQL básicas para aprovechar al máximo el uso de `mysql`.