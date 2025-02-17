# [Linux] Bash unexpand użycie: Konwertuje spacje na tabulatory

## Overview
Polecenie `unexpand` w systemie Linux służy do konwertowania spacji w plikach tekstowych na tabulatory. Jest to przydatne, gdy chcemy zredukować rozmiar pliku lub dostosować formatowanie tekstu do wymagań programów, które preferują tabulatory.

## Usage
Podstawowa składnia polecenia `unexpand` jest następująca:

```bash
unexpand [opcje] [argumenty]
```

## Common Options
- `-t, --tabs=N` - Ustawia szerokość tabulatorów na N znaków. Domyślnie jest to 8.
- `-a, --all` - Konwertuje wszystkie spacje na tabulatory, a nie tylko te, które mogą być zamienione.
- `-h, --help` - Wyświetla pomoc dotyczącą polecenia.
- `-V, --version` - Wyświetla wersję programu.

## Common Examples
1. Konwersja spacji na tabulatory w pliku `plik.txt`:
   ```bash
   unexpand plik.txt
   ```

2. Zapisanie wyniku do nowego pliku `plik_z_tabulatorami.txt`:
   ```bash
   unexpand plik.txt > plik_z_tabulatorami.txt
   ```

3. Ustawienie szerokości tabulatorów na 4 znaki:
   ```bash
   unexpand -t 4 plik.txt
   ```

4. Konwersja wszystkich spacji na tabulatory:
   ```bash
   unexpand -a plik.txt
   ```

## Tips
- Używaj opcji `-t`, aby dostosować szerokość tabulatorów do swoich potrzeb.
- Zawsze warto przetestować polecenie na kopii pliku, aby uniknąć utraty danych.
- Możesz użyć `cat -A`, aby zobaczyć, jak spacje i tabulatory są reprezentowane w pliku, co może pomóc w lepszym zrozumieniu efektów działania `unexpand`.