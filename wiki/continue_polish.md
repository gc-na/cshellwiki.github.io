# [Linux] Bash continue użycie: Kontynuowanie pętli

## Overview
Polecenie `continue` w Bashu służy do pomijania bieżącej iteracji pętli i przechodzenia do następnej. Jest to przydatne, gdy chcemy zignorować pewne warunki w trakcie wykonywania pętli.

## Usage
Podstawowa składnia polecenia `continue` jest następująca:

```bash
continue [n]
```

Gdzie `n` to opcjonalny argument, który określa, ile iteracji pętli ma zostać pominiętych.

## Common Options
- `n`: Liczba, która określa, ile iteracji należy pominąć. Domyślnie jest to 1, co oznacza, że pomijana jest tylko bieżąca iteracja.

## Common Examples

### Przykład 1: Pomijanie liczb parzystych
W tym przykładzie pomijamy wszystkie liczby parzyste w pętli `for`.

```bash
for i in {1..10}; do
    if (( i % 2 == 0 )); then
        continue
    fi
    echo $i
done
```

### Przykład 2: Pomijanie błędnych danych
W tym przykładzie pomijamy błędne dane w tablicy.

```bash
data=(1 2 "błąd" 4 5)
for item in "${data[@]}"; do
    if [[ $item == "błąd" ]]; then
        continue
    fi
    echo $item
done
```

### Przykład 3: Użycie z while
Możemy również użyć `continue` w pętli `while`.

```bash
count=0
while [ $count -lt 10 ]; do
    ((count++))
    if (( count == 5 )); then
        continue
    fi
    echo $count
done
```

## Tips
- Używaj `continue` w pętlach, aby uprościć logikę i uniknąć zagnieżdżonych instrukcji warunkowych.
- Pamiętaj, że `continue` działa tylko w kontekście pętli, więc upewnij się, że jest używane we właściwym miejscu.
- Możesz używać argumentu `n`, aby pominąć więcej niż jedną iterację, ale używaj tego ostrożnie, aby nie wprowadzić niezamierzonych błędów w logice pętli.