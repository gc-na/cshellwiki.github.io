# [Linux] C Shell (csh) helm użycie: zarządzanie aplikacjami Kubernetes

## Overview
Polecenie `helm` jest narzędziem do zarządzania aplikacjami w Kubernetes, które pozwala na łatwe instalowanie, aktualizowanie i usuwanie aplikacji w formie pakietów zwanych "chartami". Dzięki `helm` można zarządzać złożonymi aplikacjami w prosty sposób, co znacząco ułatwia pracę z Kubernetes.

## Usage
Podstawowa składnia polecenia `helm` jest następująca:

```csh
helm [options] [arguments]
```

## Common Options
Oto niektóre z najczęściej używanych opcji polecenia `helm`:

- `install`: Instaluje nową aplikację z wykresu.
- `upgrade`: Aktualizuje istniejącą aplikację do nowszej wersji.
- `uninstall`: Usuwa zainstalowaną aplikację.
- `list`: Wyświetla listę zainstalowanych aplikacji.
- `repo`: Zarządza repozytoriami chartów.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `helm`:

1. Instalacja nowej aplikacji:
   ```csh
   helm install my-app ./my-chart
   ```

2. Aktualizacja istniejącej aplikacji:
   ```csh
   helm upgrade my-app ./my-chart
   ```

3. Usunięcie zainstalowanej aplikacji:
   ```csh
   helm uninstall my-app
   ```

4. Wyświetlenie listy zainstalowanych aplikacji:
   ```csh
   helm list
   ```

5. Dodanie repozytorium chartów:
   ```csh
   helm repo add my-repo https://example.com/charts
   ```

## Tips
- Zawsze sprawdzaj dostępne wersje wykresów przed aktualizacją, aby uniknąć problemów z niekompatybilnością.
- Używaj opcji `--dry-run` podczas instalacji lub aktualizacji, aby zobaczyć, co zostanie zrobione, bez wprowadzania zmian.
- Regularnie aktualizuj swoje repozytoria chartów, aby mieć dostęp do najnowszych wersji aplikacji.