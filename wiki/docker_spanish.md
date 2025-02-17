# [Linux] Bash docker uso: Gestor de contenedores

## Overview
El comando `docker` se utiliza para gestionar contenedores, que son entornos ligeros y portables que permiten ejecutar aplicaciones de manera aislada. Docker facilita la creación, despliegue y ejecución de aplicaciones en contenedores, lo que mejora la eficiencia y la consistencia en diferentes entornos.

## Usage
La sintaxis básica del comando `docker` es la siguiente:

```bash
docker [opciones] [argumentos]
```

## Common Options
- `run`: Crea y ejecuta un contenedor a partir de una imagen.
- `ps`: Lista los contenedores en ejecución.
- `images`: Muestra las imágenes disponibles en el sistema.
- `rm`: Elimina uno o más contenedores.
- `rmi`: Elimina una o más imágenes.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `docker`:

1. **Ejecutar un contenedor de Ubuntu:**
   ```bash
   docker run -it ubuntu
   ```

2. **Listar contenedores en ejecución:**
   ```bash
   docker ps
   ```

3. **Mostrar todas las imágenes disponibles:**
   ```bash
   docker images
   ```

4. **Eliminar un contenedor específico:**
   ```bash
   docker rm nombre_del_contenedor
   ```

5. **Eliminar una imagen específica:**
   ```bash
   docker rmi nombre_de_la_imagen
   ```

## Tips
- Siempre asegúrate de que los contenedores que deseas eliminar estén detenidos para evitar errores.
- Utiliza `docker-compose` para gestionar aplicaciones que requieren múltiples contenedores.
- Mantén tus imágenes actualizadas para beneficiarte de las últimas características y parches de seguridad.
- Aprovecha los volúmenes de Docker para persistir datos entre reinicios de contenedores.