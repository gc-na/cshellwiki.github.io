# [Linux] Bash mv użycie: Przenoszenie i zmiana nazw plików

## Overview
Polecenie `mv` w systemie Linux służy do przenoszenia plików i katalogów oraz zmiany ich nazw. Jest to jedno z podstawowych poleceń w Bash, które pozwala na organizowanie i zarządzanie plikami w systemie.

## Usage
Podstawowa składnia polecenia `mv` jest następująca:

```bash
mv [opcje] [argumenty]
```

## Common Options
- `-i`: Interaktywnie, zapyta przed nadpisaniem istniejącego pliku.
- `-u`: Przenosi plik tylko wtedy, gdy źródło jest nowsze od celu lub gdy cel nie istnieje.
- `-v`: Wyświetla szczegóły operacji przenoszenia lub zmiany nazwy.
- `-n`: Nie nadpisuje istniejących plików.

## Common Examples
Przykłady użycia polecenia `mv`:

1. **Przenoszenie pliku do innego katalogu:**
   ```bash
   mv plik.txt /ścieżka/do/katalogu/
   ```

2. **Zmiana nazwy pliku:**
   ```bash
   mv stara_nazwa.txt nowa_nazwa.txt
   ```

3. **Przenoszenie wielu plików do katalogu:**
   ```bash
   mv plik1.txt plik2.txt /ścieżka/do/katalogu/
   ```

4. **Przenoszenie pliku z potwierdzeniem:**
   ```bash
   mv -i plik.txt /ścieżka/do/katalogu/
   ```

5. **Wyświetlanie szczegółów przenoszenia:**
   ```bash
   mv -v plik.txt /ścieżka/do/katalogu/
   ```

## Tips
- Zawsze używaj opcji `-i`, gdy przenosisz pliki do katalogu, w którym mogą istnieć pliki o tej samej nazwie, aby uniknąć przypadkowego nadpisania.
- Sprawdź, czy plik źródłowy istnieje przed przeniesieniem, aby uniknąć błędów.
- Możesz używać `mv` do przenoszenia plików między różnymi systemami plików, co czyni je bardzo wszechstronnym narzędziem.