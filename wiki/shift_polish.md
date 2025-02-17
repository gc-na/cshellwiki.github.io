# [Linux] Bash shift użycie: Przesuwanie argumentów w skryptach

## Overview
Polecenie `shift` w Bash służy do przesuwania argumentów pozycyjnych w skryptach. Umożliwia to usunięcie pierwszego argumentu i przesunięcie pozostałych w lewo, co jest przydatne przy przetwarzaniu argumentów w pętli.

## Usage
Podstawowa składnia polecenia `shift` jest następująca:

```bash
shift [n]
```

Gdzie `n` to liczba argumentów, o które chcesz przesunąć.

## Common Options
- `n`: Liczba argumentów do przesunięcia. Domyślnie `n` wynosi 1, co oznacza, że pierwszy argument zostanie usunięty.

## Common Examples

### Przykład 1: Proste przesunięcie
```bash
#!/bin/bash
echo "Pierwszy argument: $1"
shift
echo "Po przesunięciu, pierwszy argument: $1"
```
Wynik:
```
Pierwszy argument: arg1
Po przesunięciu, pierwszy argument: arg2
```

### Przykład 2: Przesunięcie o więcej niż jeden argument
```bash
#!/bin/bash
echo "Argumenty: $1, $2, $3"
shift 2
echo "Po przesunięciu, argumenty: $1, $2"
```
Wynik:
```
Argumenty: arg1, arg2, arg3
Po przesunięciu, argumenty: arg3, 
```

### Przykład 3: Użycie w pętli
```bash
#!/bin/bash
while [[ $# -gt 0 ]]; do
    echo "Aktualny argument: $1"
    shift
done
```
Wynik:
```
Aktualny argument: arg1
Aktualny argument: arg2
Aktualny argument: arg3
```

## Tips
- Używaj `shift` w pętli, aby łatwo przetwarzać wszystkie argumenty skryptu.
- Pamiętaj, że po przesunięciu argumentów, `$#` (liczba argumentów) zmniejsza się, co może być przydatne w warunkach pętli.
- Zawsze sprawdzaj, czy masz wystarczającą liczbę argumentów przed przesunięciem, aby uniknąć nieoczekiwanych błędów.