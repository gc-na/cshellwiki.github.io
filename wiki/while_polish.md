# [Linux] C Shell (csh) while użycie: wykonuje polecenia w pętli

## Overview
Polecenie `while` w C Shell (csh) służy do wykonywania zestawu poleceń w pętli, dopóki określony warunek jest spełniony. Jest to przydatne w sytuacjach, gdy chcemy powtarzać operacje, aż do momentu, gdy warunek przestanie być prawdziwy.

## Usage
Podstawowa składnia polecenia `while` jest następująca:

```csh
while (warunek)
    polecenie1
    polecenie2
    ...
end
```

## Common Options
Polecenie `while` w C Shell nie ma wielu opcji, ale można używać różnych warunków logicznych w celu kontrolowania pętli. Oto kilka przykładów warunków, które można stosować:

- `-eq`: równe
- `-ne`: różne
- `-lt`: mniejsze
- `-gt`: większe
- `-le`: mniejsze lub równe
- `-ge`: większe lub równe

## Common Examples

### Przykład 1: Liczenie od 1 do 5
```csh
set i = 1
while ($i <= 5)
    echo "Liczba: $i"
    @ i++
end
```

### Przykład 2: Oczekiwanie na plik
```csh
set filename = "plik.txt"
while (! -e $filename)
    echo "Czekam na plik $filename..."
    sleep 2
end
echo "Plik $filename został znaleziony!"
```

### Przykład 3: Wykonywanie polecenia do momentu spełnienia warunku
```csh
set count = 0
while ($count < 3)
    echo "To jest powtórzenie numer: $count"
    @ count++
end
```

## Tips
- Upewnij się, że warunek w pętli `while` ma szansę na spełnienie, aby uniknąć nieskończonych pętli.
- Używaj polecenia `sleep`, aby wprowadzić opóźnienie w pętli, co może być przydatne w przypadku oczekiwania na zasoby.
- Zawsze testuj swoje skrypty w bezpiecznym środowisku, aby upewnić się, że działają zgodnie z oczekiwaniami.