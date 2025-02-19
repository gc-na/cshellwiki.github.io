# [Linux] C Shell (csh) break użycie: Przerywanie pętli

## Overview
Polecenie `break` w C Shell (csh) służy do przerywania wykonywania pętli. Gdy `break` zostanie wywołane wewnątrz pętli, natychmiast kończy jej działanie i przechodzi do następnej instrukcji po pętli.

## Usage
Podstawowa składnia polecenia `break` jest następująca:

```
break [options]
```

## Common Options
Polecenie `break` w C Shell nie ma wielu opcji. Jego główną funkcją jest przerywanie pętli. Można jednak używać go w kontekście różnych typów pętli, takich jak `foreach`, `while` czy `for`.

## Common Examples

### Przykład 1: Przerwanie pętli `foreach`
```csh
foreach i (1 2 3 4 5)
    if ($i == 3) then
        break
    endif
    echo $i
end
```
W tym przykładzie pętla `foreach` wypisze liczby 1 i 2, a następnie przerwie działanie, gdy `i` osiągnie wartość 3.

### Przykład 2: Przerwanie pętli `while`
```csh
set count = 1
while ($count <= 5)
    if ($count == 4) then
        break
    endif
    echo $count
    @ count++
end
```
Tutaj pętla `while` wypisze liczby 1, 2 i 3, a następnie przerwie działanie, gdy `count` osiągnie wartość 4.

### Przykład 3: Użycie w pętli `for`
```csh
foreach num (10 20 30 40 50)
    if ($num == 30) then
        break
    endif
    echo $num
end
```
W tym przypadku pętla `foreach` wypisze 10 i 20, a następnie przerwie działanie, gdy `num` osiągnie wartość 30.

## Tips
- Używaj `break` w pętlach, gdy chcesz zakończyć ich działanie na podstawie określonego warunku.
- Pamiętaj, że `break` przerywa tylko najbliższą pętlę, w której jest wywoływane.
- Możesz zagnieżdżać pętle, ale `break` będzie działać tylko na najbliższą z nich.