# [Linux] Bash switch uso equivalente: Cambiar entre diferentes opciones

## Overview
El comando `switch` en Bash permite alternar entre diferentes opciones o condiciones en un script. Aunque no es un comando nativo de Bash, se puede simular su funcionalidad utilizando estructuras de control como `case` o `if`.

## Usage
La sintaxis básica para usar `switch` (simulado) es la siguiente:

```bash
case variable in
    patrón1)
        # comandos para patrón1
        ;;
    patrón2)
        # comandos para patrón2
        ;;
    *)
        # comandos por defecto
        ;;
esac
```

## Common Options
Aunque `switch` no tiene opciones como tal, los patrones en el comando `case` pueden incluir:

- `*`: Coincide con cualquier cadena.
- `?`: Coincide con un solo carácter.
- `[abc]`: Coincide con cualquier carácter dentro de los corchetes.

## Common Examples

### Ejemplo 1: Uso básico de `case`
```bash
read -p "Introduce un número del 1 al 3: " numero
case $numero in
    1)
        echo "Elegiste uno."
        ;;
    2)
        echo "Elegiste dos."
        ;;
    3)
        echo "Elegiste tres."
        ;;
    *)
        echo "Número no válido."
        ;;
esac
```

### Ejemplo 2: Comprobación de extensiones de archivo
```bash
archivo="documento.txt"
case $archivo in
    *.txt)
        echo "Es un archivo de texto."
        ;;
    *.jpg|*.png)
        echo "Es una imagen."
        ;;
    *)
        echo "Tipo de archivo desconocido."
        ;;
esac
```

### Ejemplo 3: Selección de opciones de menú
```bash
echo "Selecciona una opción: 1) Inicio 2) Configuración 3) Salir"
read opcion
case $opcion in
    1)
        echo "Has seleccionado Inicio."
        ;;
    2)
        echo "Has seleccionado Configuración."
        ;;
    3)
        echo "Saliendo..."
        ;;
    *)
        echo "Opción no válida."
        ;;
esac
```

## Tips
- Utiliza `case` cuando tengas múltiples condiciones que evaluar, ya que es más legible que múltiples `if`.
- Asegúrate de incluir un caso por defecto (`*`) para manejar entradas no válidas.
- Los patrones pueden ser combinados para simplificar el código, como en el ejemplo de extensiones de archivo.