# [Linux] C Shell (csh) od: wyświetlanie zawartości plików w różnych formatach

## Overview
Polecenie `od` (octal dump) służy do wyświetlania zawartości plików w różnych formatach, takich jak ósemkowy, szesnastkowy, czy tekstowy. Jest przydatne do analizy plików binarnych i tekstowych, umożliwiając użytkownikom zrozumienie ich zawartości na poziomie surowych danych.

## Usage
Podstawowa składnia polecenia `od` jest następująca:

```
od [opcje] [argumenty]
```

## Common Options
- `-A, --address-radix=RADIX` - Ustawia system liczbowy dla adresów (np. `d` dla dziesiętnego, `o` dla ósemkowego, `x` dla szesnastkowego).
- `-t, --format=TYPE` - Określa format wyjścia (np. `c` dla znaków, `d` dla dziesiętnych, `x` dla szesnastkowych).
- `-N, --read-bytes=N` - Odczytuje tylko pierwsze N bajtów z pliku.
- `-v, --output-duplicates` - Wyświetla powtarzające się wartości.

## Common Examples
1. Wyświetlenie zawartości pliku w formacie szesnastkowym:
   ```bash
   od -x plik.txt
   ```

2. Odczytanie pierwszych 16 bajtów pliku w formacie dziesiętnym:
   ```bash
   od -N 16 -t d1 plik.bin
   ```

3. Wyświetlenie zawartości pliku w formacie ósemkowym z adresami w formacie szesnastkowym:
   ```bash
   od -A x -t o1 plik.bin
   ```

4. Wyświetlenie zawartości pliku jako znaków:
   ```bash
   od -c plik.txt
   ```

## Tips
- Używaj opcji `-N`, aby ograniczyć liczbę odczytywanych bajtów, co może przyspieszyć analizę dużych plików.
- Eksperymentuj z różnymi formatami wyjścia, aby lepiej zrozumieć strukturę danych w pliku.
- Pamiętaj, że `od` jest narzędziem do analizy, więc używaj go w połączeniu z innymi poleceniami, aby uzyskać pełniejszy obraz danych.