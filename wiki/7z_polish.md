# [Linux] C Shell (csh) 7z użycie: Kompresja i dekompresja plików

## Overview
Polecenie `7z` jest narzędziem do kompresji i dekompresji plików, które obsługuje wiele formatów archiwów, w tym 7z, ZIP, RAR i inne. Umożliwia użytkownikom efektywne zarządzanie dużymi zbiorami danych poprzez ich kompresję, co oszczędza miejsce na dysku.

## Usage
Podstawowa składnia polecenia `7z` jest następująca:

```
7z [opcje] [argumenty]
```

## Common Options
- `a`: Dodaje pliki do archiwum.
- `x`: Wypakowuje pliki z archiwum.
- `t`: Określa typ archiwum (np. 7z, zip).
- `l`: Wyświetla zawartość archiwum.
- `d`: Usuwa pliki z archiwum.

## Common Examples
- **Tworzenie archiwum 7z**:
  ```bash
  7z a archiwum.7z plik1.txt plik2.txt
  ```

- **Wypakowywanie archiwum 7z**:
  ```bash
  7z x archiwum.7z
  ```

- **Wyświetlanie zawartości archiwum**:
  ```bash
  7z l archiwum.7z
  ```

- **Usuwanie pliku z archiwum**:
  ```bash
  7z d archiwum.7z plik1.txt
  ```

## Tips
- Zawsze sprawdzaj dostępne opcje za pomocą `7z -h`, aby uzyskać pełną listę funkcji.
- Używaj opcji `-p` do zabezpieczenia archiwum hasłem, co zwiększa bezpieczeństwo danych.
- Regularnie aktualizuj oprogramowanie 7z, aby korzystać z najnowszych funkcji i poprawek bezpieczeństwa.