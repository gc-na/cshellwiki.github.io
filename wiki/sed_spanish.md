# [Linux] Bash sed Uso: Herramienta para la manipulación de texto

## Overview
El comando `sed`, que significa "stream editor", es una herramienta poderosa en Bash utilizada para realizar transformaciones básicas en texto. Permite editar, buscar y reemplazar texto en archivos o flujos de datos de manera eficiente.

## Usage
La sintaxis básica del comando `sed` es la siguiente:

```bash
sed [opciones] [argumentos]
```

## Common Options
- `-e`: Permite agregar múltiples expresiones de edición.
- `-i`: Edita los archivos en su lugar (in-place), modificando el archivo original.
- `-n`: Suprime la salida automática, permitiendo mostrar solo las líneas que se especifiquen.
- `s/patrón/reemplazo/`: Realiza una sustitución del patrón por el reemplazo.

## Common Examples

### 1. Reemplazar texto en un archivo
Para reemplazar todas las ocurrencias de "manzana" por "naranja" en un archivo llamado `frutas.txt`:

```bash
sed -i 's/manzana/naranja/g' frutas.txt
```

### 2. Mostrar solo líneas que contienen un patrón
Para mostrar solo las líneas que contienen la palabra "error" en un archivo de registro:

```bash
sed -n '/error/p' registro.log
```

### 3. Eliminar líneas vacías
Para eliminar todas las líneas vacías de un archivo:

```bash
sed '/^$/d' archivo.txt
```

### 4. Cambiar el delimitador en la sustitución
Si el texto a reemplazar contiene barras (`/`), se puede usar otro delimitador, como `|`:

```bash
sed -i 's|/usr/bin|/usr/local/bin|g' rutas.txt
```

## Tips
- Siempre es recomendable hacer una copia de seguridad del archivo original antes de usar la opción `-i`.
- Puedes combinar múltiples comandos de `sed` utilizando `-e` para realizar varias ediciones en una sola ejecución.
- Usa `sed` en combinación con otros comandos de Unix, como `grep`, para un procesamiento de texto más avanzado.