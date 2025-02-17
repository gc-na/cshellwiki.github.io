# [Linux] Bash comm użycie: porównywanie plików linia po linii

## Overview
Polecenie `comm` służy do porównywania dwóch posortowanych plików tekstowych linia po linii. Umożliwia wyświetlenie linii, które są unikalne dla każdego z plików oraz linii, które są wspólne.

## Usage
Podstawowa składnia polecenia `comm` wygląda następująco:

```bash
comm [opcje] [plik1] [plik2]
```

## Common Options
- `-1`: Ukrywa linie unikalne dla pliku 1.
- `-2`: Ukrywa linie unikalne dla pliku 2.
- `-3`: Ukrywa linie wspólne.
- `-i`: Ignoruje wielkość liter podczas porównywania.
- `-u`: Wyświetla tylko unikalne linie.

## Common Examples

1. **Podstawowe porównanie dwóch plików:**
   ```bash
   comm plik1.txt plik2.txt
   ```

2. **Wyświetlenie tylko linii unikalnych dla pliku 1:**
   ```bash
   comm -13 plik1.txt plik2.txt
   ```

3. **Wyświetlenie tylko linii unikalnych dla pliku 2:**
   ```bash
   comm -12 plik1.txt plik2.txt
   ```

4. **Porównanie z ignorowaniem wielkości liter:**
   ```bash
   comm -i plik1.txt plik2.txt
   ```

5. **Wyświetlenie tylko wspólnych linii:**
   ```bash
   comm -23 plik1.txt plik2.txt
   ```

## Tips
- Upewnij się, że pliki są posortowane przed użyciem `comm`, ponieważ polecenie działa poprawnie tylko na posortowanych danych.
- Możesz użyć polecenia `sort`, aby posortować pliki przed porównaniem:
  ```bash
  sort plik1.txt > posortowany1.txt
  sort plik2.txt > posortowany2.txt
  comm posortowany1.txt posortowany2.txt
  ```
- Warto używać opcji `-i`, gdy porównujesz pliki, które mogą zawierać różnice w wielkości liter, aby uzyskać bardziej dokładne wyniki.