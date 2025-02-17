# [Linux] Bash yum użycie: Zarządzanie pakietami w systemie Linux

## Overview
Polecenie `yum` (Yellowdog Updater Modified) to narzędzie do zarządzania pakietami w systemach opartych na Red Hat, takich jak CentOS czy Fedora. Umożliwia instalację, aktualizację, usuwanie oraz zarządzanie oprogramowaniem z repozytoriów.

## Usage
Podstawowa składnia polecenia `yum` wygląda następująco:

```bash
yum [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje pakiet.
- `remove`: Usuwa pakiet.
- `update`: Aktualizuje zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety w repozytoriach.
- `info`: Wyświetla szczegóły dotyczące pakietu.
- `list`: Wyświetla listę dostępnych lub zainstalowanych pakietów.

## Common Examples
- Instalacja pakietu:
  ```bash
  yum install nazwa_pakietu
  ```

- Usunięcie pakietu:
  ```bash
  yum remove nazwa_pakietu
  ```

- Aktualizacja wszystkich zainstalowanych pakietów:
  ```bash
  yum update
  ```

- Wyszukiwanie pakietu:
  ```bash
  yum search nazwa_pakietu
  ```

- Wyświetlenie informacji o pakiecie:
  ```bash
  yum info nazwa_pakietu
  ```

- Wyświetlenie listy zainstalowanych pakietów:
  ```bash
  yum list installed
  ```

## Tips
- Zawsze warto używać opcji `-y`, aby automatycznie potwierdzać instalacje i aktualizacje, co przyspiesza proces:
  ```bash
  yum install -y nazwa_pakietu
  ```

- Regularnie aktualizuj system, aby zapewnić bezpieczeństwo i stabilność:
  ```bash
  yum update
  ```

- Sprawdzaj dostępność nowych repozytoriów, aby mieć dostęp do najnowszych pakietów i aktualizacji.