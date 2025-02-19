# [Linux] C Shell (csh) kubectl użycie: zarządzanie klastrami Kubernetes

## Overview
Polecenie `kubectl` jest narzędziem wiersza poleceń, które pozwala na interakcję z klastrami Kubernetes. Umożliwia użytkownikom zarządzanie zasobami, wdrażanie aplikacji oraz monitorowanie stanu klastra.

## Usage
Podstawowa składnia polecenia `kubectl` jest następująca:

```bash
kubectl [opcje] [argumenty]
```

## Common Options
- `get`: Pobiera informacje o zasobach w klastrze.
- `apply`: Zastosowuje zmiany w zasobach na podstawie pliku konfiguracyjnego.
- `delete`: Usuwa zasoby z klastra.
- `describe`: Wyświetla szczegółowe informacje o zasobach.
- `logs`: Wyświetla logi kontenerów w podach.

## Common Examples
- Aby uzyskać listę wszystkich podów w domyślnej przestrzeni nazw:
  ```bash
  kubectl get pods
  ```

- Aby zastosować zmiany w zasobach na podstawie pliku YAML:
  ```bash
  kubectl apply -f plik.yaml
  ```

- Aby usunąć określony pod:
  ```bash
  kubectl delete pod nazwa-podu
  ```

- Aby wyświetlić szczegóły konkretnego podu:
  ```bash
  kubectl describe pod nazwa-podu
  ```

- Aby zobaczyć logi kontenera w podzie:
  ```bash
  kubectl logs nazwa-podu
  ```

## Tips
- Używaj opcji `-n` aby wskazać konkretną przestrzeń nazw, np. `kubectl get pods -n nazwa-przestrzeni`.
- Regularnie aktualizuj swoje pliki konfiguracyjne YAML, aby uniknąć problemów z synchronizacją.
- Zawsze sprawdzaj status zasobów po zastosowaniu zmian, aby upewnić się, że wszystko działa poprawnie.