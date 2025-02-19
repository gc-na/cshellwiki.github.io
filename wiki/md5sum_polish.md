# [Linux] C Shell (csh) md5sum użycie: Obliczanie sum kontrolnych MD5

## Overview
Polecenie `md5sum` służy do obliczania sum kontrolnych MD5 dla plików. Jest to przydatne narzędzie do weryfikacji integralności danych, umożliwiające porównanie sum kontrolnych plików w celu sprawdzenia, czy nie zostały one zmienione.

## Usage
Podstawowa składnia polecenia `md5sum` jest następująca:

```csh
md5sum [opcje] [argumenty]
```

## Common Options
- `-b` : Oblicza sumę kontrolną dla plików binarnych.
- `-c` : Sprawdza sumy kontrolne z pliku.
- `-t` : Oblicza sumę kontrolną dla danych tekstowych.
- `--help` : Wyświetla pomoc dotyczącą użycia polecenia.

## Common Examples
1. Obliczanie sumy kontrolnej dla pojedynczego pliku:
   ```csh
   md5sum plik.txt
   ```

2. Obliczanie sumy kontrolnej dla wielu plików:
   ```csh
   md5sum plik1.txt plik2.txt
   ```

3. Zapisywanie sum kontrolnych do pliku:
   ```csh
   md5sum plik.txt > suma.txt
   ```

4. Sprawdzanie sum kontrolnych z pliku:
   ```csh
   md5sum -c suma.txt
   ```

## Tips
- Zawsze używaj opcji `-b` dla plików binarnych, aby uzyskać dokładne wyniki.
- Regularnie porównuj sumy kontrolne po przesyłaniu lub kopiowaniu plików, aby upewnić się, że nie uległy one zmianie.
- Użyj opcji `--help`, aby uzyskać więcej informacji na temat dostępnych opcji i ich zastosowania.