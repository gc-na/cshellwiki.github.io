# [Linux] Bash hexdump użycie: Wyświetlanie zawartości pliku w formacie szesnastkowym

## Overview
Polecenie `hexdump` służy do wyświetlania zawartości plików w formacie szesnastkowym. Umożliwia analizę danych binarnych, co jest przydatne w programowaniu i debugowaniu.

## Usage
Podstawowa składnia polecenia `hexdump` jest następująca:

```bash
hexdump [options] [arguments]
```

## Common Options
- `-C`: Wyświetla dane w formacie szesnastkowym oraz ASCII.
- `-n <bytes>`: Odczytuje tylko określoną liczbę bajtów z pliku.
- `-s <offset>`: Pomija określoną liczbę bajtów przed rozpoczęciem wyświetlania.
- `-e <format>`: Umożliwia zdefiniowanie własnego formatu wyjścia.

## Common Examples
1. Wyświetlenie zawartości pliku w formacie szesnastkowym:
   ```bash
   hexdump myfile.bin
   ```

2. Wyświetlenie zawartości pliku z formatowaniem szesnastkowym i ASCII:
   ```bash
   hexdump -C myfile.bin
   ```

3. Odczytanie tylko pierwszych 16 bajtów pliku:
   ```bash
   hexdump -n 16 myfile.bin
   ```

4. Pominięcie pierwszych 10 bajtów i wyświetlenie reszty:
   ```bash
   hexdump -s 10 myfile.bin
   ```

5. Użycie własnego formatu wyjścia:
   ```bash
   hexdump -e '16/1 "%02x " "\n"' myfile.bin
   ```

## Tips
- Używaj opcji `-C`, aby łatwiej analizować dane, widząc zarówno wartości szesnastkowe, jak i odpowiadające im znaki ASCII.
- Zawsze sprawdzaj dokumentację polecenia (`man hexdump`), aby poznać wszystkie dostępne opcje i ich zastosowanie.
- Przy dużych plikach używaj opcji `-n` i `-s`, aby ograniczyć ilość wyświetlanych danych, co ułatwi ich analizę.