# [Linux] Bash docker-compose uso: Herramienta para definir y ejecutar aplicaciones Docker

## Overview
El comando `docker-compose` es una herramienta que permite definir y ejecutar aplicaciones compuestas por múltiples contenedores Docker. Utiliza un archivo de configuración en formato YAML para especificar los servicios, redes y volúmenes necesarios para la aplicación, facilitando así la gestión de entornos complejos.

## Usage
La sintaxis básica del comando `docker-compose` es la siguiente:

```bash
docker-compose [opciones] [argumentos]
```

## Common Options
A continuación se presentan algunas de las opciones más comunes que se pueden utilizar con `docker-compose`:

- `up`: Inicia los contenedores definidos en el archivo `docker-compose.yml`.
- `down`: Detiene y elimina los contenedores, redes y volúmenes creados por `up`.
- `build`: Construye las imágenes de los servicios definidos en el archivo.
- `logs`: Muestra los registros de los contenedores en ejecución.
- `ps`: Lista los contenedores que están siendo gestionados por `docker-compose`.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `docker-compose`:

1. **Iniciar los servicios definidos**:
   ```bash
   docker-compose up
   ```

2. **Iniciar los servicios en segundo plano**:
   ```bash
   docker-compose up -d
   ```

3. **Detener y eliminar los contenedores**:
   ```bash
   docker-compose down
   ```

4. **Construir las imágenes antes de iniciar los servicios**:
   ```bash
   docker-compose up --build
   ```

5. **Ver los registros de los contenedores**:
   ```bash
   docker-compose logs
   ```

## Tips
- Asegúrate de tener un archivo `docker-compose.yml` bien configurado en el directorio donde ejecutas los comandos.
- Utiliza `docker-compose up -d` para ejecutar los contenedores en segundo plano y liberar la terminal.
- Revisa los registros con `docker-compose logs` para solucionar problemas de los servicios que no están funcionando correctamente.
- Puedes escalar servicios utilizando la opción `--scale`, por ejemplo: `docker-compose up --scale web=3` para tener tres instancias del servicio `web`.