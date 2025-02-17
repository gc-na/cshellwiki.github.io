# [Linux] Bash break użycie: Przerywanie pętli

## Overview
Polecenie `break` w Bashu jest używane do przerywania pętli, takich jak `for`, `while` czy `until`. Gdy `break` zostanie wywołane, wykonanie pętli zostaje natychmiast zatrzymane, a kontrola przechodzi do następnej instrukcji po pętli.

## Usage
Podstawowa składnia polecenia `break` jest następująca:

```bash
break [n]
```

Gdzie `n` jest opcjonalnym argumentem, który określa, ile poziomów pętli ma zostać przerwanych. Domyślnie `n` wynosi 1, co oznacza przerwanie najbliższej pętli.

## Common Options
- `n`: Liczba określająca, ile poziomów pętli ma zostać przerwanych. Na przykład, `break 2` przerwie dwie zagnieżdżone pętle.

## Common Examples

### Przykład 1: Prosta pętla for
```bash
for i in {1..5}; do
    if [ $i -eq 3 ]; then
        break
    fi
    echo "Liczba: $i"
done
```
Wynik:
```
Liczba: 1
Liczba: 2
```

### Przykład 2: Pętla while
```bash
count=1
while [ $count -le 5 ]; do
    if [ $count -eq 4 ]; then
        break
    fi
    echo "Liczba: $count"
    ((count++))
done
```
Wynik:
```
Liczba: 1
Liczba: 2
Liczba: 3
```

### Przykład 3: Zagnieżdżone pętle
```bash
for i in {1..3}; do
    for j in {1..3}; do
        if [ $j -eq 2 ]; then
            break 2
        fi
        echo "i: $i, j: $j"
    done
done
```
Wynik:
```
i: 1, j: 1
```

## Tips
- Używaj `break` w połączeniu z warunkami, aby kontrolować, kiedy pętla powinna się zakończyć.
- Pamiętaj, że `break` przerywa tylko najbliższą pętlę, chyba że podasz argument `n`.
- Staraj się unikać zbyt wielu zagnieżdżonych pętli, aby kod był bardziej czytelny i łatwiejszy do utrzymania.