# [Linux] C Shell (csh) comm: porównywanie plików tekstowych

## Overview
Polecenie `comm` służy do porównywania dwóch posortowanych plików tekstowych, wyświetlając linie, które są unikalne dla każdego pliku oraz linie wspólne. Dzięki temu można łatwo zidentyfikować różnice między dwoma zestawami danych.

## Usage
Podstawowa składnia polecenia `comm` jest następująca:

```csh
comm [opcje] [argumenty]
```

## Common Options
- `-1`: Ukrywa linie, które są unikalne dla pierwszego pliku.
- `-2`: Ukrywa linie, które są unikalne dla drugiego pliku.
- `-3`: Ukrywa linie, które są wspólne dla obu plików.
- `-i`: Ignoruje różnice w wielkości liter podczas porównywania.

## Common Examples
1. Porównanie dwóch plików i wyświetlenie wszystkich linii:
   ```csh
   comm file1.txt file2.txt
   ```

2. Wyświetlenie tylko linii unikalnych dla pierwszego pliku:
   ```csh
   comm -13 file1.txt file2.txt
   ```

3. Wyświetlenie tylko linii wspólnych dla obu plików:
   ```csh
   comm -23 file1.txt file2.txt
   ```

4. Porównanie dwóch plików z ignorowaniem wielkości liter:
   ```csh
   comm -i file1.txt file2.txt
   ```

## Tips
- Upewnij się, że pliki są posortowane przed użyciem `comm`, ponieważ polecenie działa poprawnie tylko na posortowanych danych.
- Możesz użyć polecenia `sort` w połączeniu z `comm`, aby automatycznie posortować pliki przed porównaniem:
  ```csh
  comm <(sort file1.txt) <(sort file2.txt)
  ```
- Zawsze przetestuj polecenie na małych plikach, aby upewnić się, że rozumiesz jego działanie, zanim użyjesz go na większych zbiorach danych.