# [Linux] Bash expr użycie: Obliczanie wyrażeń arytmetycznych i logicznych

## Overview
Polecenie `expr` w Bash służy do obliczania wyrażeń arytmetycznych, logicznych oraz do manipulacji tekstem. Umożliwia wykonywanie podstawowych operacji matematycznych oraz porównań.

## Usage
Podstawowa składnia polecenia `expr` wygląda następująco:

```bash
expr [opcje] [argumenty]
```

## Common Options
- `+` : Dodawanie dwóch liczb.
- `-` : Odejmowanie drugiej liczby od pierwszej.
- `*` : Mnożenie dwóch liczb (należy używać `\*` w Bash).
- `/` : Dzielenie pierwszej liczby przez drugą.
- `%` : Modulo, zwraca resztę z dzielenia.
- `=` : Porównanie równości.
- `!=` : Porównanie nierówności.
- `<` : Sprawdzenie, czy pierwsza liczba jest mniejsza od drugiej.
- `>` : Sprawdzenie, czy pierwsza liczba jest większa od drugiej.

## Common Examples
### Przykład 1: Dodawanie dwóch liczb
```bash
expr 5 + 3
```
Wynik: `8`

### Przykład 2: Odejmowanie
```bash
expr 10 - 4
```
Wynik: `6`

### Przykład 3: Mnożenie
```bash
expr 7 \* 6
```
Wynik: `42`

### Przykład 4: Dzielenie
```bash
expr 20 / 4
```
Wynik: `5`

### Przykład 5: Modulo
```bash
expr 10 % 3
```
Wynik: `1`

### Przykład 6: Porównanie
```bash
expr 5 = 5
```
Wynik: `1` (prawda)

## Tips
- Używaj `\*` zamiast `*` w poleceniach, aby uniknąć błędów związanych z interpretacją znaku mnożenia przez powłokę.
- Zawsze otaczaj argumenty z wyrażeniami w cudzysłowach, aby uniknąć problemów z białymi znakami.
- `expr` jest bardziej ograniczone w porównaniu do innych narzędzi, takich jak `bc` czy `awk`, które oferują bardziej zaawansowane funkcje matematyczne.