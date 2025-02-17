# [Linux] Bash helm użycie: zarządzanie aplikacjami Kubernetes

## Overview
Polecenie `helm` jest menedżerem pakietów dla Kubernetes, który umożliwia łatwe zarządzanie aplikacjami w klastrze Kubernetes. Dzięki Helm można instalować, aktualizować i usuwać aplikacje w formie tzw. "chartów", co znacznie ułatwia zarządzanie złożonymi aplikacjami.

## Usage
Podstawowa składnia polecenia `helm` jest następująca:

```bash
helm [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje nowy chart.
- `upgrade`: Aktualizuje istniejący chart do nowszej wersji.
- `uninstall`: Usuwa zainstalowany chart.
- `list`: Wyświetla listę zainstalowanych chartów.
- `repo`: Zarządza repozytoriami chartów.

## Common Examples
1. Instalacja nowego chartu:
   ```bash
   helm install my-release my-chart
   ```

2. Aktualizacja istniejącego chartu:
   ```bash
   helm upgrade my-release my-chart
   ```

3. Usunięcie zainstalowanego chartu:
   ```bash
   helm uninstall my-release
   ```

4. Wyświetlenie listy zainstalowanych chartów:
   ```bash
   helm list
   ```

5. Dodanie repozytorium chartów:
   ```bash
   helm repo add my-repo https://my-repo-url
   ```

## Tips
- Zawsze sprawdzaj dostępne wersje chartów przed ich instalacją, aby upewnić się, że używasz najnowszej wersji.
- Używaj opcji `--dry-run`, aby przetestować instalację lub aktualizację chartu bez wprowadzania zmian w klastrze.
- Regularnie aktualizuj swoje repozytoria chartów, aby mieć dostęp do najnowszych aplikacji i poprawek.