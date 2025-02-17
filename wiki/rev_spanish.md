# [Linux] Bash rev: Invertir líneas de texto

## Overview
El comando `rev` se utiliza para invertir el orden de los caracteres en cada línea de un archivo o entrada estándar. Es una herramienta sencilla pero útil para manipular texto en la línea de comandos.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
rev [opciones] [archivo]
```

## Common Options
- `-o, --output=FILE`: Especifica un archivo de salida donde se guardará el resultado.
- `-h, --help`: Muestra la ayuda del comando y sale.
- `-V, --version`: Muestra la versión del comando.

## Common Examples

### Invertir texto desde un archivo
Para invertir el contenido de un archivo llamado `texto.txt`, puedes usar el siguiente comando:

```bash
rev texto.txt
```

### Invertir texto desde la entrada estándar
Si deseas invertir texto que introduces manualmente, puedes usar `echo` junto con `rev`:

```bash
echo "Hola Mundo" | rev
```

### Guardar la salida en un archivo
Para guardar el resultado de la inversión en un nuevo archivo llamado `invertido.txt`, puedes usar la opción `-o`:

```bash
rev -o invertido.txt texto.txt
```

### Invertir varias líneas
Si tienes varias líneas de texto en un archivo y quieres invertir cada línea, simplemente ejecuta:

```bash
rev archivo_multilineas.txt
```

## Tips
- Utiliza `rev` en combinación con otros comandos de Unix para crear scripts más complejos.
- Recuerda que `rev` invierte los caracteres de cada línea, no el orden de las líneas en sí.
- Puedes usar `cat` para visualizar el contenido de un archivo antes de invertirlo, así puedes verificar el resultado más fácilmente.