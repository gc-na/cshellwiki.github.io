# [Linux] Bash cd użycie: Zmiana katalogu roboczego

## Overview
Polecenie `cd` (change directory) w systemie Bash służy do zmiany bieżącego katalogu roboczego. Umożliwia użytkownikom nawigację po systemie plików, co jest kluczowe dla wykonywania innych poleceń w odpowiednich lokalizacjach.

## Usage
Podstawowa składnia polecenia `cd` jest następująca:

```
cd [opcje] [argumenty]
```

## Common Options
- `..` - Przechodzi do katalogu nadrzędnego.
- `-` - Przechodzi do poprzedniego katalogu.
- `~` - Przechodzi do katalogu domowego użytkownika.

## Common Examples
- Aby przejść do katalogu nadrzędnego:
  ```bash
  cd ..
  ```

- Aby przejść do katalogu domowego:
  ```bash
  cd ~
  ```

- Aby przejść do poprzedniego katalogu:
  ```bash
  cd -
  ```

- Aby przejść do konkretnego katalogu, na przykład do katalogu "Dokumenty":
  ```bash
  cd ~/Dokumenty
  ```

- Aby przejść do katalogu o pełnej ścieżce:
  ```bash
  cd /usr/local/bin
  ```

## Tips
- Używaj `cd -`, aby szybko wrócić do ostatniego katalogu, w którym pracowałeś.
- Możesz używać autouzupełniania, naciskając klawisz Tab, aby szybko uzupełnić nazwy katalogów.
- Zawsze sprawdzaj, w jakim katalogu się znajdujesz, używając polecenia `pwd`, aby uniknąć pomyłek.