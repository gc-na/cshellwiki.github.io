# [Linux] Bash foreach użycie: Iteracja przez elementy

## Overview
Polecenie `foreach` w Bashu jest używane do iteracji przez zestaw elementów, umożliwiając wykonywanie poleceń dla każdego z nich. Jest to przydatne w sytuacjach, gdy chcemy wykonać tę samą operację na wielu plikach lub danych.

## Usage
Podstawowa składnia polecenia `foreach` wygląda następująco:

```bash
foreach [elementy] [polecenie]
```

## Common Options
Polecenie `foreach` w Bashu nie ma wielu opcji, ponieważ jest to prosty mechanizm iteracji. Jednak warto zwrócić uwagę na kilka aspektów:

- `-n` – nie wyświetlaj wyników na standardowym wyjściu.
- `-p` – pozwala na interaktywne wprowadzanie poleceń dla każdego elementu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `foreach`:

### Przykład 1: Iteracja przez pliki
```bash
foreach file in *.txt
    echo "Przetwarzam plik: $file"
end
```
W tym przykładzie polecenie wypisuje nazwę każdego pliku z rozszerzeniem `.txt`.

### Przykład 2: Prosta operacja na liczbach
```bash
foreach i (1 2 3 4 5)
    echo "Liczba: $i"
end
```
Tutaj `foreach` iteruje przez liczby od 1 do 5 i wypisuje je na ekranie.

### Przykład 3: Usuwanie plików
```bash
foreach file in *.log
    rm $file
end
```
W tym przypadku polecenie `foreach` usuwa wszystkie pliki z rozszerzeniem `.log`.

## Tips
- Używaj `foreach` w skryptach, aby uprościć operacje na wielu elementach.
- Zawsze upewnij się, że masz kopię zapasową danych przed wykonaniem operacji, które mogą je usunąć.
- Testuj swoje skrypty na małych zestawach danych, aby upewnić się, że działają zgodnie z oczekiwaniami.