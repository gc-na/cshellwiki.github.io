# [Linux] Bash fold uso: Ajustar el ancho de las líneas de texto

## Overview
El comando `fold` se utiliza en Bash para ajustar el ancho de las líneas de texto. Permite dividir líneas largas en varias más cortas, lo que facilita la lectura y la visualización en terminales con un ancho limitado.

## Usage
La sintaxis básica del comando `fold` es la siguiente:

```bash
fold [opciones] [archivo]
```

Si no se especifica un archivo, `fold` leerá desde la entrada estándar.

## Common Options
- `-w, --width=N`: Establece el ancho máximo de las líneas a N caracteres.
- `-s, --spaces`: Divide las líneas en espacios en lugar de cortar en medio de una palabra.
- `-b, --bytes`: Cuenta el ancho en bytes en lugar de caracteres.

## Common Examples

1. **Ajustar el ancho de una línea a 50 caracteres:**

```bash
fold -w 50 archivo.txt
```

2. **Dividir líneas en espacios:**

```bash
fold -s -w 30 archivo.txt
```

3. **Contar el ancho en bytes y ajustar a 40 bytes:**

```bash
fold -b -w 40 archivo.txt
```

4. **Usar fold con entrada estándar:**

```bash
echo "Este es un ejemplo de una línea muy larga que necesita ser ajustada." | fold -w 20
```

## Tips
- Utiliza la opción `-s` si deseas evitar cortar palabras, lo que mejora la legibilidad del texto.
- Experimenta con diferentes anchos para encontrar el que mejor se adapte a tu terminal o dispositivo.
- Puedes combinar `fold` con otros comandos como `cat` o `grep` para procesar texto de manera más efectiva.