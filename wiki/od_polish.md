# [Linux] Bash od: wyświetlanie zawartości plików w różnych formatach

## Overview
Polecenie `od` (octal dump) służy do wyświetlania zawartości plików w różnych formatach, takich jak ósemkowy, szesnastkowy, czy tekstowy. Umożliwia analizę danych binarnych oraz tekstowych w sposób, który ułatwia ich interpretację.

## Usage
Podstawowa składnia polecenia `od` jest następująca:

```bash
od [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `od`:

- `-A, --address-radix=RADIX` – Ustawia podstawę adresów (np. d dla dziesiętnego, o dla ósemkowego, x dla szesnastkowego).
- `-t, --format=FORMAT` – Umożliwia określenie formatu wyjścia (np. c dla znaków, d dla liczb dziesiętnych, x dla liczb szesnastkowych).
- `-N, --read-bytes=N` – Odczytuje tylko pierwsze N bajtów pliku.
- `-v, --output-duplicates` – Wyświetla duplikaty w wyjściu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `od`:

1. Wyświetlenie zawartości pliku w formacie szesnastkowym:

   ```bash
   od -t x1 plik.txt
   ```

2. Odczytanie pierwszych 16 bajtów pliku:

   ```bash
   od -N 16 plik.bin
   ```

3. Wyświetlenie zawartości pliku w formacie znakowym:

   ```bash
   od -t c plik.txt
   ```

4. Wyświetlenie adresów w formacie dziesiętnym:

   ```bash
   od -A d plik.bin
   ```

## Tips
- Używaj opcji `-N`, aby ograniczyć ilość odczytywanych danych, co może być przydatne przy dużych plikach.
- Eksperymentuj z różnymi formatami wyjścia, aby lepiej zrozumieć strukturę danych w plikach binarnych.
- Pamiętaj, że `od` jest szczególnie przydatne w analizie plików binarnych, takich jak obrazy czy pliki wykonywalne.