# [Linux] C Shell (csh) minikube użycie: Uruchamianie lokalnych klastrów Kubernetes

## Overview
Minikube to narzędzie, które umożliwia uruchamianie lokalnych klastrów Kubernetes. Jest idealne do testowania i rozwoju aplikacji w środowisku Kubernetes bez potrzeby korzystania z zewnętrznych zasobów chmurowych.

## Usage
Podstawowa składnia polecenia minikube wygląda następująco:

```csh
minikube [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla minikube:

- `start` - Uruchamia nowy klaster minikube.
- `stop` - Zatrzymuje działający klaster minikube.
- `delete` - Usuwa klaster minikube.
- `status` - Wyświetla status aktualnego klastra.
- `dashboard` - Otwiera interfejs użytkownika Kubernetes w przeglądarce.

## Common Examples
Oto kilka praktycznych przykładów użycia minikube:

1. Uruchomienie nowego klastra:
   ```csh
   minikube start
   ```

2. Sprawdzenie statusu klastra:
   ```csh
   minikube status
   ```

3. Zatrzymanie klastra:
   ```csh
   minikube stop
   ```

4. Usunięcie klastra:
   ```csh
   minikube delete
   ```

5. Otworzenie dashboardu Kubernetes:
   ```csh
   minikube dashboard
   ```

## Tips
- Upewnij się, że masz zainstalowane wszystkie wymagane zależności przed uruchomieniem minikube.
- Regularnie sprawdzaj status klastra, aby upewnić się, że działa poprawnie.
- Korzystaj z opcji `--driver` podczas uruchamiania, aby wybrać preferowany silnik wirtualizacji, np. `--driver=virtualbox`.