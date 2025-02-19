# [Linux] C Shell (csh) cp użycie: Kopiowanie plików i katalogów

## Overview
Polecenie `cp` w C Shell (csh) służy do kopiowania plików i katalogów. Umożliwia użytkownikom tworzenie kopii plików w tym samym lub innym katalogu.

## Usage
Podstawowa składnia polecenia `cp` jest następująca:

```csh
cp [opcje] [argumenty]
```

## Common Options
- `-i`: Interaktywnie pyta przed nadpisaniem istniejącego pliku.
- `-r`: Rekursywnie kopiuje katalogi i ich zawartość.
- `-u`: Kopiuje tylko wtedy, gdy źródło jest nowsze niż cel lub cel nie istnieje.
- `-v`: Wyświetla szczegóły operacji kopiowania.

## Common Examples
1. Kopiowanie pliku do innego katalogu:
   ```csh
   cp plik.txt /ścieżka/do/katalogu/
   ```

2. Kopiowanie pliku i nadpisywanie bez pytania:
   ```csh
   cp -f plik.txt /ścieżka/do/katalogu/
   ```

3. Rekursywne kopiowanie katalogu:
   ```csh
   cp -r katalog/ /ścieżka/do/katalogu/
   ```

4. Interaktywne kopiowanie z pytaniem o nadpisanie:
   ```csh
   cp -i plik.txt /ścieżka/do/katalogu/
   ```

5. Kopiowanie tylko nowszych plików:
   ```csh
   cp -u plik.txt /ścieżka/do/katalogu/
   ```

## Tips
- Zawsze używaj opcji `-i`, gdy kopiujesz pliki do katalogów, w których mogą już istnieć pliki o tej samej nazwie, aby uniknąć przypadkowego nadpisania.
- Przy kopiowaniu dużych katalogów użyj opcji `-v`, aby śledzić postęp operacji.
- Regularnie twórz kopie zapasowe ważnych plików, korzystając z `cp`, aby zabezpieczyć swoje dane.