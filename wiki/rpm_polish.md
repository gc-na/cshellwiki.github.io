# [Linux] C Shell (csh) rpm użycie: zarządzanie pakietami RPM

## Overview
Polecenie `rpm` jest narzędziem do zarządzania pakietami w systemach opartych na Red Hat, takich jak Fedora czy CentOS. Umożliwia instalację, usuwanie, aktualizację oraz sprawdzanie pakietów RPM.

## Usage
Podstawowa składnia polecenia `rpm` jest następująca:

```bash
rpm [options] [arguments]
```

## Common Options
- `-i` : Instalacja nowego pakietu.
- `-e` : Usunięcie zainstalowanego pakietu.
- `-U` : Aktualizacja zainstalowanego pakietu do nowszej wersji.
- `-q` : Zapytanie o informacje na temat zainstalowanego pakietu.
- `--help` : Wyświetlenie pomocy dotyczącej użycia polecenia.

## Common Examples
1. **Instalacja pakietu:**
   ```bash
   rpm -i nazwa_pakietu.rpm
   ```

2. **Usunięcie pakietu:**
   ```bash
   rpm -e nazwa_pakietu
   ```

3. **Aktualizacja pakietu:**
   ```bash
   rpm -U nazwa_pakietu.rpm
   ```

4. **Sprawdzenie zainstalowanego pakietu:**
   ```bash
   rpm -q nazwa_pakietu
   ```

5. **Wyświetlenie pomocy:**
   ```bash
   rpm --help
   ```

## Tips
- Zawsze sprawdzaj zależności przed instalacją pakietu, aby uniknąć problemów z brakującymi bibliotekami.
- Używaj opcji `-q` z `-l`, aby zobaczyć, jakie pliki są zainstalowane w danym pakiecie:
  ```bash
  rpm -ql nazwa_pakietu
  ```
- Regularnie aktualizuj system, aby mieć najnowsze poprawki bezpieczeństwa i funkcjonalności.