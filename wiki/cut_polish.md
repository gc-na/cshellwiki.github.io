# [Linux] Bash cut użycie: Wyodrębnianie fragmentów tekstu

## Overview
Polecenie `cut` w systemie Linux służy do wyodrębniania fragmentów tekstu z plików lub danych wejściowych. Umożliwia selekcję określonych kolumn lub znaków, co jest przydatne w obróbce danych.

## Usage
Podstawowa składnia polecenia `cut` wygląda następująco:

```bash
cut [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `cut`:

- `-f`: Wybiera określone pola (kolumny) z danych.
- `-d`: Ustala separator, który oddziela pola (domyślnie to tabulator).
- `-c`: Wybiera określone znaki z wierszy.
- `--complement`: Zwraca wszystkie pola z wyjątkiem tych określonych.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `cut`:

1. Wyodrębnianie drugiego pola z pliku, gdzie pola są oddzielone przecinkami:
   ```bash
   cut -d ',' -f 2 plik.txt
   ```

2. Wyodrębnianie pierwszych 10 znaków z pliku:
   ```bash
   cut -c 1-10 plik.txt
   ```

3. Wyodrębnianie wielu pól (1 i 3) z pliku, gdzie pola są oddzielone tabulatorami:
   ```bash
   cut -f 1,3 plik.txt
   ```

4. Użycie `cut` w połączeniu z `echo`:
   ```bash
   echo "jeden,dwa,trzy" | cut -d ',' -f 2
   ```

## Tips
- Używaj opcji `-d` do określenia separatora, aby dostosować `cut` do różnych formatów plików.
- Możesz łączyć `cut` z innymi poleceniami, takimi jak `grep` czy `sort`, aby uzyskać bardziej zaawansowane operacje na danych.
- Sprawdzaj wyniki polecenia na małych próbkach danych przed zastosowaniem go na większych plikach, aby upewnić się, że działa zgodnie z oczekiwaniami.