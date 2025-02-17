# [Linux] Bash psql Uso: Interactuar con bases de datos PostgreSQL

## Overview
El comando `psql` es una herramienta de línea de comandos para interactuar con bases de datos PostgreSQL. Permite a los usuarios ejecutar consultas SQL, administrar bases de datos y realizar tareas de mantenimiento.

## Usage
La sintaxis básica del comando `psql` es la siguiente:

```bash
psql [opciones] [argumentos]
```

## Common Options
- `-h`: Especifica el host del servidor de la base de datos.
- `-p`: Define el puerto del servidor de la base de datos.
- `-U`: Indica el nombre de usuario para conectarse a la base de datos.
- `-d`: Especifica el nombre de la base de datos a la que se desea conectar.
- `-c`: Permite ejecutar un comando SQL directamente desde la línea de comandos.

## Common Examples
1. **Conectar a una base de datos:**
   ```bash
   psql -U usuario -d basededatos
   ```

2. **Ejecutar un comando SQL directamente:**
   ```bash
   psql -U usuario -d basededatos -c "SELECT * FROM tabla;"
   ```

3. **Conectar a un servidor remoto:**
   ```bash
   psql -h servidor.com -p 5432 -U usuario -d basededatos
   ```

4. **Listar todas las bases de datos:**
   ```bash
   psql -U usuario -c "\l"
   ```

5. **Salir de psql:**
   ```bash
   \q
   ```

## Tips
- Utiliza el comando `\?` dentro de `psql` para obtener ayuda sobre los comandos disponibles.
- Guarda tus consultas SQL en archivos y ejecútalas usando `psql -f archivo.sql` para facilitar la gestión de scripts.
- Asegúrate de tener los permisos adecuados en la base de datos para evitar errores de acceso.