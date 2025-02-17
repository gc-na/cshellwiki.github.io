# [Linux] Bash if użycie: Sprawdzanie warunków w skryptach

## Overview
Polecenie `if` w Bashu służy do wykonywania różnych działań w zależności od spełnienia określonych warunków. Umożliwia to podejmowanie decyzji w skryptach, co jest kluczowe w automatyzacji zadań.

## Usage
Podstawowa składnia polecenia `if` jest następująca:

```bash
if [ warunek ]; then
    # polecenia do wykonania, jeśli warunek jest prawdziwy
fi
```

## Common Options
- `-e`: Sprawdza, czy plik istnieje.
- `-d`: Sprawdza, czy podana ścieżka jest katalogiem.
- `-f`: Sprawdza, czy podana ścieżka jest plikiem.
- `-z`: Sprawdza, czy zmienna jest pusta.
- `-n`: Sprawdza, czy zmienna nie jest pusta.

## Common Examples

### Przykład 1: Sprawdzenie istnienia pliku
```bash
if [ -e "plik.txt" ]; then
    echo "Plik istnieje."
else
    echo "Plik nie istnieje."
fi
```

### Przykład 2: Sprawdzenie, czy zmienna jest pusta
```bash
zmienna=""
if [ -z "$zmienna" ]; then
    echo "Zmienna jest pusta."
else
    echo "Zmienna nie jest pusta."
fi
```

### Przykład 3: Sprawdzenie, czy katalog istnieje
```bash
if [ -d "/ścieżka/do/katalogu" ]; then
    echo "Katalog istnieje."
else
    echo "Katalog nie istnieje."
fi
```

### Przykład 4: Użycie wielu warunków
```bash
if [ -f "plik.txt" ] && [ -r "plik.txt" ]; then
    echo "Plik istnieje i jest czytelny."
else
    echo "Plik nie istnieje lub nie jest czytelny."
fi
```

## Tips
- Zawsze używaj spacji wokół nawiasów kwadratowych, aby uniknąć błędów składniowych.
- Możesz zagnieżdżać instrukcje `if`, aby sprawdzać bardziej złożone warunki.
- Używaj `elif` do sprawdzania dodatkowych warunków, co pozwala na bardziej złożoną logikę w skryptach.