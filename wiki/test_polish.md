# [Linux] Bash test użycie: Sprawdzanie warunków

## Overview
Polecenie `test` w Bashu służy do oceny warunków i zwraca wartość prawda (0) lub fałsz (1) w zależności od wyniku tej oceny. Jest często używane w skryptach do podejmowania decyzji na podstawie różnych warunków, takich jak istnienie plików, porównania liczb czy sprawdzanie typów danych.

## Usage
Podstawowa składnia polecenia `test` wygląda następująco:

```bash
test [opcje] [argumenty]
```

Można również użyć skróconej formy z nawiasami kwadratowymi:

```bash
[ opcje ]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `test`:

- `-e [plik]`: Sprawdza, czy plik istnieje.
- `-f [plik]`: Sprawdza, czy plik jest regularnym plikiem.
- `-d [katalog]`: Sprawdza, czy katalog istnieje.
- `-z [string]`: Sprawdza, czy długość łańcucha jest równa zeru.
- `-n [string]`: Sprawdza, czy długość łańcucha jest większa od zera.
- `[liczba1] -eq [liczba2]`: Sprawdza, czy liczby są równe.
- `[liczba1] -lt [liczba2]`: Sprawdza, czy liczba1 jest mniejsza od liczby2.

## Common Examples

### Sprawdzanie istnienia pliku
```bash
test -e plik.txt && echo "Plik istnieje."
```

### Sprawdzanie, czy jest to katalog
```bash
test -d /ścieżka/do/katalogu && echo "To jest katalog."
```

### Porównanie dwóch liczb
```bash
a=5
b=10
test $a -lt $b && echo "$a jest mniejsze od $b."
```

### Sprawdzanie długości łańcucha
```bash
string=""
test -z "$string" && echo "Łańcuch jest pusty."
```

## Tips
- Używaj nawiasów kwadratowych `[` i `]` dla lepszej czytelności, ale pamiętaj, aby dodać spacje przed i po nawiasach.
- Możesz łączyć kilka warunków w jednym poleceniu, używając operatorów `&&` (i) oraz `||` (lub).
- W skryptach, zamiast używać `test`, możesz użyć `[[ ... ]]`, co oferuje bardziej zaawansowane możliwości, takie jak porównania wzorców.