# [Linux] Bash while użycie: Wykonywanie pętli do momentu spełnienia warunku

## Overview
Polecenie `while` w Bashu służy do wykonywania bloku kodu tak długo, jak długo określony warunek jest spełniony. Jest to przydatne w sytuacjach, gdy chcemy powtarzać operacje, dopóki nie zajdzie zmiana w stanie lub wartości.

## Usage
Podstawowa składnia polecenia `while` wygląda następująco:

```bash
while [warunek]; do
    # komendy do wykonania
done
```

## Common Options
Polecenie `while` nie ma wielu opcji, ale oto kilka ważnych aspektów, które warto znać:

- `-n`: Sprawdza, czy długość ciągu jest różna od zera.
- `-z`: Sprawdza, czy długość ciągu jest równa zeru.

## Common Examples

### Przykład 1: Liczenie od 1 do 5
```bash
count=1
while [ $count -le 5 ]; do
    echo "Liczba: $count"
    ((count++))
done
```

### Przykład 2: Odczyt z pliku linia po linii
```bash
while IFS= read -r line; do
    echo "Linia: $line"
done < plik.txt
```

### Przykład 3: Pętla nieskończona z warunkiem przerwania
```bash
while true; do
    echo "Naciśnij q, aby zakończyć."
    read -r input
    if [ "$input" = "q" ]; then
        break
    fi
done
```

## Tips
- Używaj `break` do przerywania pętli, gdy warunek nie jest już spełniony.
- Zawsze upewnij się, że warunek w pętli `while` ma szansę na spełnienie, aby uniknąć pętli nieskończonej.
- Możesz używać `sleep` w pętli, aby ograniczyć obciążenie CPU, gdy pętla wykonuje się często.