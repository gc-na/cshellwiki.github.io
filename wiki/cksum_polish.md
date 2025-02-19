# [Linux] C Shell (csh) cksum: obliczanie sum kontrolnych plików

## Overview
Polecenie `cksum` w powłoce C Shell (csh) służy do obliczania sum kontrolnych plików. Generuje ono wartość kontrolną oraz liczbę bajtów w pliku, co może być przydatne do sprawdzania integralności danych.

## Usage
Podstawowa składnia polecenia `cksum` jest następująca:

```csh
cksum [opcje] [argumenty]
```

## Common Options
- `-a, --algorithm=ALG`: Używa określonego algorytmu do obliczenia sumy kontrolnej (np. md5).
- `-h, --help`: Wyświetla pomoc dotyczącą użycia polecenia.
- `-V, --version`: Wyświetla wersję programu.

## Common Examples
1. Obliczanie sumy kontrolnej dla pojedynczego pliku:
   ```csh
   cksum plik.txt
   ```

2. Obliczanie sum kontrolnych dla wielu plików:
   ```csh
   cksum plik1.txt plik2.txt plik3.txt
   ```

3. Użycie opcji do wyświetlenia wersji:
   ```csh
   cksum -V
   ```

4. Obliczanie sumy kontrolnej z użyciem algorytmu md5:
   ```csh
   cksum -a md5 plik.txt
   ```

## Tips
- Używaj `cksum` do porównywania plików po ich przesyłaniu lub kopiowaniu, aby upewnić się, że nie uległy one zmianie.
- Możesz zapisać wyniki `cksum` do pliku, używając przekierowania:
  ```csh
  cksum plik.txt > suma.txt
  ```
- Pamiętaj, że różne systemy operacyjne mogą generować różne sumy kontrolne dla tych samych plików, dlatego zawsze sprawdzaj zgodność z dokumentacją.