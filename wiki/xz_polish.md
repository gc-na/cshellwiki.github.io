# [Linux] Bash xz Użycie: Kompresja i dekompresja plików

## Overview
Polecenie `xz` służy do kompresji i dekompresji plików przy użyciu algorytmu LZMA. Jest to narzędzie, które pozwala na znaczną redukcję rozmiaru plików, co jest szczególnie przydatne w przypadku dużych zbiorów danych.

## Usage
Podstawowa składnia polecenia `xz` jest następująca:

```bash
xz [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `xz`:

- `-d`, `--decompress`: dekompresuje plik.
- `-k`, `--keep`: zachowuje oryginalny plik po kompresji.
- `-v`, `--verbose`: wyświetla szczegółowe informacje o procesie kompresji.
- `-f`, `--force`: wymusza nadpisanie istniejących plików.
- `-9`: ustawia maksymalny poziom kompresji (od 1 do 9).

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `xz`:

1. Kompresja pliku:
   ```bash
   xz plik.txt
   ```

2. Dekomprensja pliku:
   ```bash
   xz -d plik.txt.xz
   ```

3. Kompresja pliku z zachowaniem oryginału:
   ```bash
   xz -k plik.txt
   ```

4. Wyświetlenie szczegółowych informacji podczas kompresji:
   ```bash
   xz -v plik.txt
   ```

5. Wymuszenie nadpisania istniejącego pliku:
   ```bash
   xz -f plik.txt
   ```

## Tips
- Używaj opcji `-k`, jeśli chcesz zachować oryginalne pliki po kompresji.
- Zwróć uwagę na poziom kompresji; wyższy poziom (np. `-9`) może zająć więcej czasu, ale skutkuje mniejszym rozmiarem pliku.
- Regularnie sprawdzaj, czy masz zainstalowaną najnowszą wersję `xz`, aby korzystać z najnowszych funkcji i poprawek.