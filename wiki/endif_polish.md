# [Linux] Bash endif użycie: Zakończenie bloku warunkowego

## Overview
Polecenie `endif` w Bashu jest używane do kończenia bloku warunkowego, który został rozpoczęty za pomocą polecenia `if`. Jest to część składni warunkowej, która pozwala na wykonywanie różnych działań w zależności od spełnienia określonych warunków.

## Usage
Podstawowa składnia polecenia `endif` jest następująca:

```bash
endif
```

## Common Options
Polecenie `endif` nie ma żadnych opcji, ponieważ jest to jedynie znacznik końca bloku warunkowego.

## Common Examples

### Przykład 1: Prosty blok warunkowy
```bash
if [ -f "plik.txt" ]; then
    echo "Plik istnieje."
endif
```

### Przykład 2: Blok warunkowy z innym warunkiem
```bash
if [ "$USER" == "admin" ]; then
    echo "Masz uprawnienia administratora."
else
    echo "Nie masz uprawnień administratora."
endif
```

### Przykład 3: Zagnieżdżony blok warunkowy
```bash
if [ -d "katalog" ]; then
    echo "Katalog istnieje."
    if [ "$(ls -A katalog)" ]; then
        echo "Katalog nie jest pusty."
    else
        echo "Katalog jest pusty."
    endif
else
    echo "Katalog nie istnieje."
endif
```

## Tips
- Upewnij się, że każde polecenie `if` ma odpowiadające mu `endif`, aby uniknąć błędów składniowych.
- Używaj wcięć w zagnieżdżonych blokach warunkowych, aby poprawić czytelność kodu.
- Zawsze testuj warunki przed ich użyciem, aby upewnić się, że działają zgodnie z oczekiwaniami.