# [Linux] C Shell (csh) foreach użycie: Iteracja przez elementy listy

## Overview
Polecenie `foreach` w C Shell (csh) służy do iteracji przez elementy listy. Umożliwia wykonywanie określonego bloku kodu dla każdego elementu w podanej liście, co jest przydatne w automatyzacji zadań.

## Usage
Podstawowa składnia polecenia `foreach` jest następująca:

```
foreach zmienna (lista)
    komendy
end
```

## Common Options
Polecenie `foreach` nie ma wielu opcji, ale oto kilka, które mogą być przydatne:
- `zmienna`: zmienna, która przyjmuje wartość każdego elementu z listy.
- `lista`: lista elementów, przez które chcemy iterować.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `foreach`:

### Przykład 1: Iteracja przez liczby
```csh
foreach i (1 2 3 4 5)
    echo "Liczba: $i"
end
```
Ten przykład wyświetli liczby od 1 do 5.

### Przykład 2: Iteracja przez pliki
```csh
foreach file (*.txt)
    echo "Znaleziony plik: $file"
end
```
Tutaj polecenie wyświetli wszystkie pliki z rozszerzeniem `.txt` w bieżącym katalogu.

### Przykład 3: Wykonywanie polecenia na plikach
```csh
foreach file (*.log)
    gzip $file
end
```
W tym przykładzie każde wystąpienie pliku `.log` zostanie skompresowane przy użyciu `gzip`.

## Tips
- Używaj `foreach` w skryptach, aby uprościć powtarzające się zadania.
- Upewnij się, że lista elementów jest poprawnie sformatowana, aby uniknąć błędów.
- Możesz zagnieżdżać polecenia `foreach`, aby iterować przez złożone struktury danych.