# [Linux] Bash printf użycie: Formatowanie i wyświetlanie tekstu

## Overview
Polecenie `printf` w Bashu służy do formatowania i wyświetlania tekstu na standardowym wyjściu. Jest to bardziej zaawansowana wersja polecenia `echo`, która umożliwia precyzyjne kontrolowanie formatu wyjścia.

## Usage
Podstawowa składnia polecenia `printf` jest następująca:

```bash
printf [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `printf`:

- `-v` : Przypisuje sformatowany tekst do zmiennej.
- `-f` : Umożliwia użycie formatu specyfikacji.
- `--help` : Wyświetla pomoc dotyczącą użycia polecenia.

## Common Examples

### Przykład 1: Proste wyświetlenie tekstu
```bash
printf "Witaj, świecie!\n"
```

### Przykład 2: Formatowanie liczb
```bash
printf "Liczba: %d\n" 42
```

### Przykład 3: Wyświetlanie z wypełnieniem
```bash
printf "|%10s|\n" "tekst"
```

### Przykład 4: Przypisanie do zmiennej
```bash
printf -v zmienna "Wartość: %s" "test"
echo "$zmienna"
```

### Przykład 5: Użycie wielu argumentów
```bash
printf "Imię: %s, Wiek: %d\n" "Jan" 30
```

## Tips
- Używaj `\n` do dodawania nowych linii w wyjściu.
- Zawsze sprawdzaj, czy odpowiedni format specyfikacji jest użyty dla typów danych, aby uniknąć błędów.
- Możesz używać `printf` w skryptach do generowania bardziej złożonych raportów i formatów wyjściowych.