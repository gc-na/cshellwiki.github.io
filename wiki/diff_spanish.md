# [Linux] Bash diff uso equivalente: Comparar archivos y mostrar diferencias

## Overview
El comando `diff` se utiliza en Bash para comparar el contenido de dos archivos de texto y mostrar las diferencias entre ellos. Es una herramienta muy útil para desarrolladores y administradores de sistemas que necesitan identificar cambios en archivos de configuración, código fuente, o cualquier otro tipo de documento.

## Usage
La sintaxis básica del comando `diff` es la siguiente:

```bash
diff [opciones] [archivo1] [archivo2]
```

## Common Options
- `-u`: Muestra las diferencias en formato unificado, que es más fácil de leer.
- `-c`: Muestra las diferencias en formato de contexto, proporcionando más información sobre el contexto de las líneas cambiadas.
- `-i`: Ignora las diferencias entre mayúsculas y minúsculas.
- `-w`: Ignora los espacios en blanco al comparar las líneas.
- `-r`: Compara directorios de manera recursiva.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `diff`:

1. Comparar dos archivos de texto:
   ```bash
   diff archivo1.txt archivo2.txt
   ```

2. Mostrar diferencias en formato unificado:
   ```bash
   diff -u archivo1.txt archivo2.txt
   ```

3. Comparar dos directorios recursivamente:
   ```bash
   diff -r directorio1/ directorio2/
   ```

4. Ignorar espacios en blanco al comparar:
   ```bash
   diff -w archivo1.txt archivo2.txt
   ```

5. Mostrar diferencias en formato de contexto:
   ```bash
   diff -c archivo1.txt archivo2.txt
   ```

## Tips
- Utiliza la opción `-u` para obtener un formato de salida más legible, especialmente útil al revisar cambios en código.
- Cuando compares directorios, la opción `-r` es muy efectiva para ver todas las diferencias en archivos anidados.
- Si trabajas en un entorno colaborativo, considera usar `diff` junto con herramientas de control de versiones como Git para gestionar cambios de manera más eficiente.