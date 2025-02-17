# [Linux] Bash yum uso: Gestión de paquetes en sistemas basados en RPM

## Overview
El comando `yum` (Yellowdog Updater Modified) es una herramienta de gestión de paquetes para sistemas operativos basados en RPM (Red Hat Package Manager). Permite a los usuarios instalar, actualizar, eliminar y gestionar paquetes de software de manera sencilla y eficiente.

## Usage
La sintaxis básica del comando `yum` es la siguiente:

```bash
yum [opciones] [argumentos]
```

## Common Options
- `install`: Instala uno o más paquetes.
- `remove`: Elimina uno o más paquetes.
- `update`: Actualiza todos los paquetes instalados a la última versión disponible.
- `search`: Busca paquetes que coincidan con el término especificado.
- `info`: Muestra información detallada sobre un paquete específico.
- `list`: Lista todos los paquetes disponibles o instalados.

## Common Examples
Aquí tienes algunos ejemplos prácticos del uso de `yum`:

- **Instalar un paquete**:
  ```bash
  yum install nombre_del_paquete
  ```

- **Eliminar un paquete**:
  ```bash
  yum remove nombre_del_paquete
  ```

- **Actualizar todos los paquetes**:
  ```bash
  yum update
  ```

- **Buscar un paquete**:
  ```bash
  yum search nombre_del_paquete
  ```

- **Obtener información sobre un paquete**:
  ```bash
  yum info nombre_del_paquete
  ```

- **Listar todos los paquetes instalados**:
  ```bash
  yum list installed
  ```

## Tips
- Siempre es recomendable ejecutar `yum update` regularmente para mantener tu sistema y paquetes al día.
- Utiliza `yum clean all` para limpiar la caché y liberar espacio en disco.
- Antes de eliminar un paquete, verifica las dependencias que podrían verse afectadas.
- Puedes usar `yum history` para ver un registro de las transacciones realizadas con `yum`, lo que puede ser útil para deshacer cambios si es necesario.