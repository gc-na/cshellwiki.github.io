# [Linux] Bash pacman użycie: Zarządzanie pakietami w systemie Arch Linux

## Overview
Polecenie `pacman` jest menedżerem pakietów używanym w systemie Arch Linux oraz jego pochodnych. Umożliwia instalację, aktualizację i usuwanie pakietów oprogramowania, a także zarządzanie zależnościami.

## Usage
Podstawowa składnia polecenia `pacman` wygląda następująco:

```bash
pacman [opcje] [argumenty]
```

## Common Options
- `-S`: Instalacja pakietu.
- `-R`: Usunięcie pakietu.
- `-U`: Instalacja pakietu z lokalnego pliku.
- `-Sy`: Synchronizacja bazy danych pakietów.
- `-Syu`: Aktualizacja systemu i pakietów.
- `-Q`: Zapytanie o zainstalowane pakiety.

## Common Examples
- Instalacja pakietu:
  ```bash
  pacman -S nazwa_pakietu
  ```

- Usunięcie pakietu:
  ```bash
  pacman -R nazwa_pakietu
  ```

- Aktualizacja wszystkich zainstalowanych pakietów:
  ```bash
  pacman -Syu
  ```

- Instalacja pakietu z lokalnego pliku:
  ```bash
  pacman -U /ścieżka/do/pakietu.pkg.tar.zst
  ```

- Wyświetlenie listy zainstalowanych pakietów:
  ```bash
  pacman -Q
  ```

## Tips
- Zawsze używaj opcji `-Sy` przed instalacją nowych pakietów, aby upewnić się, że baza danych jest aktualna.
- Regularnie aktualizuj system za pomocą `pacman -Syu`, aby mieć najnowsze wersje oprogramowania.
- Używaj `pacman -Rns nazwa_pakietu`, aby usunąć pakiet oraz jego nieużywane zależności.