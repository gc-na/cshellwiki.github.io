# [Linux] Bash paste Uso: Combina líneas de archivos

## Overview
El comando `paste` en Bash se utiliza para combinar líneas de varios archivos de texto. Une las líneas correspondientes de cada archivo en una sola línea, separándolas por un delimitador, que por defecto es una tabulación. Es útil para fusionar datos de diferentes fuentes en un formato más legible.

## Usage
La sintaxis básica del comando `paste` es la siguiente:

```bash
paste [opciones] [archivos]
```

## Common Options
- `-d DELIM`: Especifica un delimitador diferente al predeterminado (tabulación) para separar las líneas.
- `-s`: Combina las líneas de un solo archivo en lugar de hacerlo por columnas.
- `-z`: Usa un delimitador nulo en lugar de una nueva línea al final de cada archivo.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `paste`:

1. **Combinar dos archivos por columnas**:
   ```bash
   paste archivo1.txt archivo2.txt
   ```

2. **Usar un delimitador personalizado**:
   ```bash
   paste -d ',' archivo1.txt archivo2.txt
   ```

3. **Combinar líneas de un solo archivo**:
   ```bash
   paste -s archivo1.txt
   ```

4. **Combinar múltiples archivos con un delimitador diferente**:
   ```bash
   paste -d '|' archivo1.txt archivo2.txt archivo3.txt
   ```

5. **Combinar archivos y usar un delimitador nulo**:
   ```bash
   paste -z archivo1.txt archivo2.txt
   ```

## Tips
- Siempre verifica el contenido de los archivos antes de combinarlos para asegurarte de que tengan el mismo número de líneas si deseas una combinación precisa.
- Experimenta con diferentes delimitadores para mejorar la legibilidad de los datos combinados.
- Usa la opción `-s` cuando necesites un formato más compacto, especialmente si trabajas con un solo archivo.