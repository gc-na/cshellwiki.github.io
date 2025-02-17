# [Linux] Bash dnf użycie: Zarządzanie pakietami w systemie

## Overview
Polecenie `dnf` (Dandified YUM) jest menedżerem pakietów dla systemów opartych na Red Hat, takich jak Fedora i CentOS. Umożliwia instalację, aktualizację i usuwanie pakietów oprogramowania, a także zarządzanie repozytoriami.

## Usage
Podstawowa składnia polecenia `dnf` jest następująca:

```bash
dnf [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje pakiet.
- `remove`: Usuwa pakiet.
- `update`: Aktualizuje zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety w repozytoriach.
- `list`: Wyświetla listę dostępnych lub zainstalowanych pakietów.
- `info`: Wyświetla szczegółowe informacje o pakiecie.

## Common Examples
- Instalacja pakietu:
  ```bash
  dnf install nazwa_pakietu
  ```

- Usuwanie pakietu:
  ```bash
  dnf remove nazwa_pakietu
  ```

- Aktualizacja wszystkich zainstalowanych pakietów:
  ```bash
  dnf update
  ```

- Wyszukiwanie pakietu:
  ```bash
  dnf search nazwa_pakietu
  ```

- Wyświetlanie informacji o pakiecie:
  ```bash
  dnf info nazwa_pakietu
  ```

## Tips
- Zawsze warto używać opcji `-y`, aby automatycznie potwierdzić instalację lub usunięcie pakietów, co przyspiesza proces:
  ```bash
  dnf install -y nazwa_pakietu
  ```

- Regularnie aktualizuj system, aby zapewnić bezpieczeństwo i stabilność:
  ```bash
  dnf update
  ```

- Używaj opcji `list installed`, aby sprawdzić, które pakiety są aktualnie zainstalowane:
  ```bash
  dnf list installed
  ```