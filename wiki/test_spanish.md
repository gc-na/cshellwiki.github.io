# [Linux] Bash test uso: Evaluar expresiones y condiciones

## Overview
El comando `test` en Bash se utiliza para evaluar expresiones y condiciones. Permite comprobar el estado de archivos, comparar cadenas y realizar evaluaciones numéricas. Es una herramienta fundamental en scripts para tomar decisiones basadas en condiciones.

## Usage
La sintaxis básica del comando `test` es la siguiente:

```bash
test [opciones] [argumentos]
```

## Common Options
- `-e archivo`: Verifica si el archivo existe.
- `-f archivo`: Comprueba si el archivo es un archivo regular.
- `-d directorio`: Verifica si el directorio existe.
- `-z cadena`: Comprueba si la longitud de la cadena es cero.
- `-n cadena`: Verifica si la longitud de la cadena es mayor que cero.
- `==`: Compara dos cadenas para ver si son iguales.
- `-lt`: Compara si un número es menor que otro.
- `-gt`: Compara si un número es mayor que otro.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `test`:

1. **Verificar si un archivo existe:**
   ```bash
   test -e archivo.txt && echo "El archivo existe."
   ```

2. **Comprobar si una cadena está vacía:**
   ```bash
   cadena=""
   test -z "$cadena" && echo "La cadena está vacía."
   ```

3. **Comparar dos números:**
   ```bash
   num1=5
   num2=10
   test $num1 -lt $num2 && echo "$num1 es menor que $num2."
   ```

4. **Verificar si un directorio existe:**
   ```bash
   test -d /ruta/al/directorio && echo "El directorio existe."
   ```

5. **Comprobar si dos cadenas son iguales:**
   ```bash
   cadena1="hola"
   cadena2="hola"
   test "$cadena1" == "$cadena2" && echo "Las cadenas son iguales."
   ```

## Tips
- Utiliza `[[ ... ]]` en lugar de `test` para una sintaxis más moderna y flexible en Bash.
- Agrupa condiciones con `&&` y `||` para crear evaluaciones más complejas.
- Recuerda siempre usar comillas alrededor de las variables para evitar problemas con espacios en blanco.