# [Linux] Bash sqlite3 Uso: Interactuar con bases de datos SQLite

## Overview
El comando `sqlite3` se utiliza para interactuar con bases de datos SQLite desde la línea de comandos. Permite crear, modificar y consultar bases de datos de manera sencilla y eficiente.

## Usage
La sintaxis básica del comando `sqlite3` es la siguiente:

```bash
sqlite3 [opciones] [argumentos]
```

## Common Options
- `-help`: Muestra la ayuda y las opciones disponibles.
- `-version`: Muestra la versión de SQLite.
- `-init <archivo>`: Ejecuta comandos SQL desde un archivo al iniciar la sesión.
- `-batch`: Ejecuta en modo por lotes, ideal para scripts.
- `-echo`: Muestra las consultas SQL antes de ejecutarlas.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `sqlite3`:

### Crear una nueva base de datos
```bash
sqlite3 mi_base_de_datos.db
```

### Crear una tabla
```bash
sqlite3 mi_base_de_datos.db "CREATE TABLE usuarios (id INTEGER PRIMARY KEY, nombre TEXT, edad INTEGER);"
```

### Insertar datos en la tabla
```bash
sqlite3 mi_base_de_datos.db "INSERT INTO usuarios (nombre, edad) VALUES ('Juan', 30);"
```

### Consultar datos de la tabla
```bash
sqlite3 mi_base_de_datos.db "SELECT * FROM usuarios;"
```

### Exportar datos a un archivo CSV
```bash
sqlite3 -header -csv mi_base_de_datos.db "SELECT * FROM usuarios;" > usuarios.csv
```

## Tips
- Utiliza el modo `-batch` para ejecutar scripts sin interacción manual.
- Siempre realiza copias de seguridad de tus bases de datos antes de realizar cambios importantes.
- Aprovecha el uso de archivos de inicialización para cargar configuraciones y datos al iniciar `sqlite3`.