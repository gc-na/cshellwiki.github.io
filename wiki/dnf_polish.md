# [Linux] C Shell (csh) dnf użycie: Zarządzanie pakietami w systemie

## Overview
Polecenie `dnf` (Dandified YUM) jest menedżerem pakietów dla systemów opartych na Red Hat, takich jak Fedora i CentOS. Umożliwia instalację, aktualizację i usuwanie pakietów oprogramowania, a także zarządzanie ich zależnościami.

## Usage
Podstawowa składnia polecenia `dnf` jest następująca:

```bash
dnf [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje pakiet.
- `remove`: Usuwa zainstalowany pakiet.
- `update`: Aktualizuje zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety według nazwy lub opisu.
- `list`: Wyświetla listę dostępnych lub zainstalowanych pakietów.

## Common Examples
- Instalacja pakietu:
  ```bash
  dnf install nazwa_pakietu
  ```

- Usunięcie pakietu:
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

- Wyświetlanie listy zainstalowanych pakietów:
  ```bash
  dnf list installed
  ```

## Tips
- Zawsze sprawdzaj dostępność aktualizacji przed instalacją nowych pakietów, aby uniknąć problemów z zależnościami.
- Używaj opcji `-y`, aby automatycznie potwierdzać instalację lub usunięcie pakietów, co przyspiesza proces.
- Regularnie przeglądaj zainstalowane pakiety i usuwaj te, które nie są już potrzebne, aby zaoszczędzić miejsce na dysku.