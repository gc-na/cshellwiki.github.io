# [Linux] Bash helm uso: Gestionar paquetes de Kubernetes

## Overview
El comando `helm` es una herramienta de gestión de paquetes para Kubernetes que permite a los usuarios definir, instalar y actualizar aplicaciones en clústeres de Kubernetes. Facilita la implementación de aplicaciones complejas mediante el uso de "charts", que son colecciones de archivos que describen un conjunto relacionado de recursos de Kubernetes.

## Usage
La sintaxis básica del comando `helm` es la siguiente:

```bash
helm [opciones] [argumentos]
```

## Common Options
- `install`: Instala un chart en un clúster de Kubernetes.
- `upgrade`: Actualiza una instalación existente de un chart.
- `uninstall`: Desinstala un chart de un clúster de Kubernetes.
- `list`: Muestra las instalaciones de charts en el clúster.
- `repo`: Gestiona los repositorios de charts.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso del comando `helm`:

### Instalar un chart
```bash
helm install mi-aplicacion stable/mi-chart
```

### Actualizar un chart
```bash
helm upgrade mi-aplicacion stable/mi-chart
```

### Desinstalar un chart
```bash
helm uninstall mi-aplicacion
```

### Listar instalaciones de charts
```bash
helm list
```

### Añadir un repositorio de charts
```bash
helm repo add mi-repo https://mi-repo.com/charts
```

## Tips
- Asegúrate de mantener tus repositorios de charts actualizados utilizando `helm repo update`.
- Utiliza `helm search repo` para buscar charts disponibles en tus repositorios.
- Revisa la documentación de cada chart para entender las configuraciones y opciones disponibles antes de la instalación.