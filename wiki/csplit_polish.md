# [Linux] Bash csplit użycie: Dzieli plik na mniejsze części

## Overview
Polecenie `csplit` służy do dzielenia plików tekstowych na mniejsze fragmenty na podstawie wzorców lub liczby linii. Jest to przydatne, gdy chcemy podzielić duży plik na mniejsze, bardziej zarządzalne części.

## Usage
Podstawowa składnia polecenia `csplit` jest następująca:

```bash
csplit [opcje] [argumenty]
```

## Common Options
- `-f, --prefix=PREFIX` - Określa prefiks dla nazw plików wynikowych.
- `-n, --digits=N` - Ustala liczbę cyfr w numeracji plików wynikowych.
- `-b, --suffix-format=FORMAT` - Określa format sufiksu dla plików wynikowych.
- `-k, --keep-files` - Zachowuje pliki wynikowe, nawet jeśli są puste.

## Common Examples

1. **Podział pliku na 10-liniowe fragmenty:**
   ```bash
   csplit myfile.txt 10
   ```

2. **Podział pliku na podstawie wzorca:**
   ```bash
   csplit myfile.txt /Wzorzec/ {99}
   ```
   W tym przykładzie plik zostanie podzielony w miejscach, gdzie występuje "Wzorzec", a maksymalna liczba fragmentów to 99.

3. **Użycie prefiksu dla plików wynikowych:**
   ```bash
   csplit -f fragment_ myfile.txt 10
   ```
   Pliki wynikowe będą miały prefiks "fragment_", np. "fragment_00", "fragment_01", itd.

4. **Zachowanie pustych plików:**
   ```bash
   csplit -k myfile.txt /Wzorzec/
   ```

## Tips
- Używaj opcji `-n` do dostosowania liczby cyfr w nazwach plików, aby uniknąć problemów z nazwami plików w przypadku dużej liczby fragmentów.
- Sprawdź zawartość plików wynikowych po podziale, aby upewnić się, że podział został przeprowadzony zgodnie z oczekiwaniami.
- Eksperymentuj z różnymi wzorcami, aby dostosować podział do swoich potrzeb.