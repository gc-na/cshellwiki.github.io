# [Linux] Bash minikube uso: Herramienta para ejecutar Kubernetes localmente

## Overview
El comando `minikube` permite a los desarrolladores ejecutar un clúster de Kubernetes localmente en su máquina. Es una herramienta útil para probar aplicaciones en un entorno de Kubernetes sin necesidad de un clúster completo en la nube.

## Usage
La sintaxis básica del comando es la siguiente:

```bash
minikube [opciones] [argumentos]
```

## Common Options
- `start`: Inicia un clúster de Minikube.
- `stop`: Detiene el clúster de Minikube en ejecución.
- `status`: Muestra el estado actual del clúster de Minikube.
- `delete`: Elimina el clúster de Minikube.
- `kubectl`: Permite ejecutar comandos de Kubernetes directamente en el clúster de Minikube.

## Common Examples
Aquí hay algunos ejemplos prácticos de cómo usar el comando `minikube`:

1. **Iniciar un clúster de Minikube**:
   ```bash
   minikube start
   ```

2. **Detener el clúster de Minikube**:
   ```bash
   minikube stop
   ```

3. **Ver el estado del clúster**:
   ```bash
   minikube status
   ```

4. **Eliminar el clúster de Minikube**:
   ```bash
   minikube delete
   ```

5. **Ejecutar un comando de Kubernetes**:
   ```bash
   minikube kubectl -- get pods
   ```

## Tips
- Asegúrate de tener suficiente memoria y CPU asignadas a Minikube para evitar problemas de rendimiento.
- Utiliza `minikube dashboard` para abrir una interfaz gráfica que te permita gestionar tu clúster de manera más visual.
- Considera usar complementos de Minikube para extender su funcionalidad, como `minikube addons enable metrics-server` para habilitar el servidor de métricas.