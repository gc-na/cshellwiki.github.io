# [Linux] Bash tr <Uso equivalente en español>: Transformar caracteres en texto

## Overview
El comando `tr` en Bash se utiliza para traducir o eliminar caracteres en un flujo de texto. Es especialmente útil para manipular datos en scripts o en la línea de comandos.

## Usage
La sintaxis básica del comando `tr` es la siguiente:

```bash
tr [opciones] [argumentos]
```

## Common Options
- `-d`: Elimina los caracteres especificados.
- `-s`: Suprime las repeticiones de caracteres adyacentes.
- `-c`: Complementa el conjunto de caracteres especificado.
- `-t`: Limita la traducción a un conjunto de caracteres específico.

## Common Examples
1. **Convertir minúsculas a mayúsculas**:
   ```bash
   echo "hola mundo" | tr 'a-z' 'A-Z'
   ```
   Este comando convierte todas las letras minúsculas en mayúsculas.

2. **Eliminar espacios en blanco**:
   ```bash
   echo "hola   mundo" | tr -d ' '
   ```
   Aquí se eliminan todos los espacios en blanco del texto.

3. **Suprimir caracteres repetidos**:
   ```bash
   echo "hooolaaa   muundo" | tr -s 'o ' 'o '
   ```
   Este comando suprime las repeticiones de 'o' y los espacios.

4. **Reemplazar caracteres**:
   ```bash
   echo "123-456-789" | tr '-' ':'
   ```
   En este caso, se reemplazan los guiones por dos puntos.

## Tips
- Utiliza `tr` en combinación con otros comandos como `grep` o `sort` para realizar tareas más complejas.
- Recuerda que `tr` trabaja con flujos de texto, así que es ideal para usar en tuberías.
- Siempre prueba tus comandos con datos de ejemplo antes de aplicarlos a archivos importantes.