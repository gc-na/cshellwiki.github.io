# [Linux] Bash kubectl uso: Interactuar con clústeres de Kubernetes

## Overview
El comando `kubectl` es la herramienta de línea de comandos para interactuar con clústeres de Kubernetes. Permite a los usuarios desplegar aplicaciones, gestionar recursos y obtener información sobre el estado de los clústeres.

## Usage
La sintaxis básica del comando `kubectl` es la siguiente:

```bash
kubectl [options] [arguments]
```

## Common Options
- `get`: Recupera información sobre recursos en el clúster.
- `apply`: Aplica cambios a los recursos definidos en archivos de configuración.
- `delete`: Elimina recursos del clúster.
- `describe`: Muestra detalles sobre un recurso específico.
- `logs`: Muestra los registros de un pod.

## Common Examples
Aquí hay algunos ejemplos prácticos de cómo usar `kubectl`:

1. **Listar todos los pods en el clúster:**
   ```bash
   kubectl get pods
   ```

2. **Aplicar un archivo de configuración YAML:**
   ```bash
   kubectl apply -f deployment.yaml
   ```

3. **Eliminar un pod específico:**
   ```bash
   kubectl delete pod nombre-del-pod
   ```

4. **Describir un servicio:**
   ```bash
   kubectl describe service nombre-del-servicio
   ```

5. **Ver los registros de un pod:**
   ```bash
   kubectl logs nombre-del-pod
   ```

## Tips
- Siempre verifica el estado de tus recursos después de aplicar cambios usando `kubectl get`.
- Utiliza `kubectl explain [resource]` para obtener más información sobre un recurso específico y sus campos.
- Considera usar contextos y configuraciones de kubeconfig para gestionar múltiples clústeres de manera eficiente.