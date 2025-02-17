# [Linux] Bash kubectl Użycie: zarządzanie klastrami Kubernetes

## Overview
`kubectl` to narzędzie wiersza poleceń, które umożliwia interakcję z klastrami Kubernetes. Umożliwia użytkownikom zarządzanie aplikacjami uruchomionymi w klastrze, a także monitorowanie i konfigurowanie zasobów.

## Usage
Podstawowa składnia polecenia `kubectl` jest następująca:

```bash
kubectl [opcje] [argumenty]
```

## Common Options
- `get`: Pobiera informacje o zasobach.
- `describe`: Wyświetla szczegółowe informacje o zasobach.
- `apply`: Zastosowuje zmiany w zasobach z pliku konfiguracyjnego.
- `delete`: Usuwa zasoby z klastra.
- `logs`: Wyświetla logi kontenera.

## Common Examples
1. **Pobieranie listy podów:**
   ```bash
   kubectl get pods
   ```

2. **Wyświetlanie szczegółów konkretnego poda:**
   ```bash
   kubectl describe pod [nazwa-poda]
   ```

3. **Zastosowanie zmian z pliku YAML:**
   ```bash
   kubectl apply -f [plik.yaml]
   ```

4. **Usuwanie poda:**
   ```bash
   kubectl delete pod [nazwa-poda]
   ```

5. **Wyświetlanie logów kontenera:**
   ```bash
   kubectl logs [nazwa-poda]
   ```

## Tips
- Używaj `kubectl get all`, aby uzyskać przegląd wszystkich zasobów w klastrze.
- Zawsze sprawdzaj status zasobów po zastosowaniu zmian, używając `kubectl get [typ-zasobu]`.
- Możesz używać aliasów w Bashu, aby skrócić polecenia, np. `alias k=kubectl`.