# [Linux] Bash kubectl Uso: Interactuar con clústeres de Kubernetes

## Overview
El comando `kubectl` es la herramienta de línea de comandos para interactuar con clústeres de Kubernetes. Permite a los usuarios desplegar aplicaciones, gestionar recursos y obtener información sobre el estado del clúster.

## Usage
La sintaxis básica del comando `kubectl` es la siguiente:

```bash
kubectl [opciones] [argumentos]
```

## Common Options
- `get`: Recupera información sobre recursos en el clúster.
- `apply`: Aplica cambios a los recursos utilizando archivos de configuración.
- `delete`: Elimina recursos del clúster.
- `describe`: Muestra detalles sobre un recurso específico.
- `logs`: Muestra los registros de un pod.

## Common Examples
Aquí hay algunos ejemplos prácticos del uso de `kubectl`:

1. **Obtener todos los pods en el clúster:**
   ```bash
   kubectl get pods
   ```

2. **Aplicar un archivo de configuración:**
   ```bash
   kubectl apply -f archivo-configuracion.yaml
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
- Utiliza el comando `kubectl get all` para obtener una vista general de todos los recursos en el clúster.
- Asegúrate de tener configurado el contexto correcto si trabajas con múltiples clústeres.
- Usa `kubectl --help` para obtener más información sobre las opciones y comandos disponibles.