# [Linux] Bash else użycie: Wykonywanie alternatywnych poleceń

## Overview
Polecenie `else` w Bashu jest częścią struktury warunkowej, która pozwala na wykonanie alternatywnego bloku kodu, gdy warunek w instrukcji `if` nie zostanie spełniony. Umożliwia to tworzenie bardziej złożonych skryptów, które mogą reagować na różne sytuacje.

## Usage
Podstawowa składnia polecenia `else` jest następująca:

```bash
if [ warunek ]; then
    # kod do wykonania, gdy warunek jest prawdziwy
else
    # kod do wykonania, gdy warunek jest fałszywy
fi
```

## Common Options
Polecenie `else` nie ma opcji, ponieważ jest to część struktury kontrolnej. Wszystkie opcje i argumenty dotyczące `if` są stosowane w kontekście całej instrukcji warunkowej.

## Common Examples

### Przykład 1: Prosta instrukcja warunkowa
```bash
if [ -f "plik.txt" ]; then
    echo "Plik istnieje."
else
    echo "Plik nie istnieje."
fi
```

### Przykład 2: Sprawdzenie zmiennej
```bash
liczba=10

if [ $liczba -gt 5 ]; then
    echo "Liczba jest większa niż 5."
else
    echo "Liczba jest mniejsza lub równa 5."
fi
```

### Przykład 3: Użycie z wieloma warunkami
```bash
if [ $1 -eq 1 ]; then
    echo "Argument to 1."
else
    echo "Argument to nie 1."
fi
```

## Tips
- Używaj `else` w połączeniu z `if`, aby tworzyć bardziej złożone logiki w swoich skryptach.
- Pamiętaj o zakończeniu bloku `if` słowem kluczowym `fi`, aby uniknąć błędów składniowych.
- Możesz zagnieżdżać instrukcje `if` i `else`, aby obsługiwać bardziej skomplikowane warunki.