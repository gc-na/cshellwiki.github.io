# [Linux] C Shell (csh) split użycie: Dzieli pliki na mniejsze części

## Overview
Polecenie `split` w C Shell (csh) służy do dzielenia dużych plików na mniejsze fragmenty. Jest to przydatne, gdy chcemy ułatwić przesyłanie lub przetwarzanie dużych zbiorów danych.

## Usage
Podstawowa składnia polecenia `split` wygląda następująco:

```
split [opcje] [argumenty]
```

## Common Options
- `-l NUM` - dzieli plik na części zawierające NUM linii każda.
- `-b SIZE` - dzieli plik na części o rozmiarze SIZE (np. 10k dla 10 kilobajtów).
- `-d` - używa cyfr do nazewnictwa plików wyjściowych zamiast domyślnych liter.
- `--additional-suffix=SUFFIX` - dodaje określony SUFFIX do nazw plików wyjściowych.

## Common Examples
1. Dzielenie pliku na części po 1000 linii:
   ```csh
   split -l 1000 duzy_plik.txt
   ```

2. Dzielenie pliku na części o rozmiarze 1MB:
   ```csh
   split -b 1m duzy_plik.txt
   ```

3. Użycie cyfr do nazewnictwa plików:
   ```csh
   split -d -l 500 duzy_plik.txt
   ```

4. Dzielenie pliku z dodatkowym sufiksem:
   ```csh
   split --additional-suffix=.txt -l 2000 duzy_plik.txt czesc_
   ```

## Tips
- Zawsze sprawdzaj rozmiar i liczbę linii w pliku przed podziałem, aby lepiej dostosować opcje.
- Używaj opcji `-d`, jeśli potrzebujesz łatwiejszego dostępu do poszczególnych części pliku.
- Pamiętaj, że domyślne nazwy plików są generowane w kolejności alfabetycznej, co może być pomocne w organizacji.