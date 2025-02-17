# [Linux] Bash bzip2 Użycie: Kompresja plików

## Overview
Bzip2 to narzędzie służące do kompresji plików, które wykorzystuje algorytm Burrows-Wheeler. Jest znane z wysokiego stopnia kompresji, co czyni je popularnym wyborem do archiwizacji danych.

## Usage
Podstawowa składnia polecenia bzip2 jest następująca:

```bash
bzip2 [opcje] [argumenty]
```

## Common Options
- `-d`, `--decompress`: Dekompresuje plik.
- `-k`, `--keep`: Zachowuje oryginalny plik po kompresji.
- `-f`, `--force`: Wymusza nadpisanie istniejących plików.
- `-v`, `--verbose`: Wyświetla szczegółowe informacje o postępie kompresji.
- `-z`, `--compress`: Kompresuje plik (domyślna opcja).

## Common Examples
- Kompresja pliku:
  ```bash
  bzip2 plik.txt
  ```

- Dekompresja pliku:
  ```bash
  bzip2 -d plik.txt.bz2
  ```

- Kompresja pliku z zachowaniem oryginału:
  ```bash
  bzip2 -k plik.txt
  ```

- Wymuszenie nadpisania istniejącego pliku:
  ```bash
  bzip2 -f plik.txt
  ```

- Wyświetlenie szczegółowych informacji podczas kompresji:
  ```bash
  bzip2 -v plik.txt
  ```

## Tips
- Używaj opcji `-k`, aby uniknąć przypadkowego usunięcia oryginalnych plików.
- Sprawdzaj rozmiar plików przed i po kompresji, aby ocenić skuteczność.
- Bzip2 jest bardziej efektywny w kompresji dużych plików, więc warto go używać w przypadku archiwizacji większych zbiorów danych.