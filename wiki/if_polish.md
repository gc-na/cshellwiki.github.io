# [Linux] C Shell (csh) if: Sprawdzanie warunków

## Overview
Polecenie `if` w C Shell (csh) służy do wykonywania warunkowego kodu w skryptach. Pozwala na sprawdzenie, czy dany warunek jest spełniony, a następnie wykonanie odpowiednich poleceń w zależności od wyniku tego sprawdzenia.

## Usage
Podstawowa składnia polecenia `if` jest następująca:

```csh
if (warunek) then
    polecenia
endif
```

## Common Options
- `then`: Słowo kluczowe, które rozpoczyna blok poleceń do wykonania, jeśli warunek jest prawdziwy.
- `endif`: Słowo kluczowe, które kończy blok `if`.

## Common Examples

### Przykład 1: Sprawdzenie zmiennej
```csh
set x = 5
if ($x == 5) then
    echo "x jest równe 5"
endif
```

### Przykład 2: Sprawdzenie pliku
```csh
if (-e "plik.txt") then
    echo "Plik istnieje"
else
    echo "Plik nie istnieje"
endif
```

### Przykład 3: Sprawdzenie katalogu
```csh
if (-d "katalog") then
    echo "To jest katalog"
else
    echo "To nie jest katalog"
endif
```

## Tips
- Używaj odpowiednich operatorów porównania, takich jak `==` dla porównania wartości oraz `-e` dla sprawdzenia istnienia pliku.
- Zawsze zamykaj blok `if` słowem kluczowym `endif`, aby uniknąć błędów w skryptach.
- Możesz zagnieżdżać bloki `if`, aby sprawdzać wiele warunków w jednym skrypcie.