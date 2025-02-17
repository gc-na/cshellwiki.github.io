# [Linux] Bash minikube użycie: Uruchamianie lokalnych klastrów Kubernetes

## Overview
Minikube to narzędzie, które umożliwia uruchamianie lokalnych klastrów Kubernetes. Jest szczególnie przydatne dla deweloperów, którzy chcą testować aplikacje w środowisku Kubernetes bez potrzeby korzystania z zewnętrznych zasobów.

## Usage
Podstawowa składnia polecenia minikube jest następująca:

```bash
minikube [opcje] [argumenty]
```

## Common Options
- `start` - Rozpoczyna nowy klaster Minikube.
- `stop` - Zatrzymuje działający klaster Minikube.
- `delete` - Usuwa klaster Minikube.
- `status` - Wyświetla status klastra Minikube.
- `kubectl` - Umożliwia korzystanie z narzędzia kubectl w kontekście klastra Minikube.

## Common Examples
1. **Uruchomienie nowego klastra Minikube:**
   ```bash
   minikube start
   ```

2. **Sprawdzenie statusu klastra:**
   ```bash
   minikube status
   ```

3. **Zatrzymanie klastra:**
   ```bash
   minikube stop
   ```

4. **Usunięcie klastra:**
   ```bash
   minikube delete
   ```

5. **Uruchomienie polecenia kubectl w kontekście Minikube:**
   ```bash
   minikube kubectl -- get pods -A
   ```

## Tips
- Upewnij się, że masz zainstalowane wszystkie wymagane zależności, takie jak VirtualBox lub Docker, przed uruchomieniem Minikube.
- Regularnie sprawdzaj status klastra, aby upewnić się, że działa poprawnie.
- Używaj opcji `--driver` podczas uruchamiania klastra, aby określić preferowany silnik wirtualizacji, np. `minikube start --driver=docker`.