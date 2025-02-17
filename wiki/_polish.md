# [Linux] Bash @ echo: wyświetlanie tekstu w terminalu

## Overview
Polecenie `echo` w Bashu służy do wyświetlania tekstu lub zmiennych w terminalu. Jest to jedno z najprostszych i najczęściej używanych poleceń w skryptach oraz interakcji z użytkownikiem.

## Usage
Podstawowa składnia polecenia `echo` jest następująca:

```bash
echo [opcje] [argumenty]
```

## Common Options
- `-n`: Nie dodaje znaku nowej linii na końcu.
- `-e`: Włącza interpretację sekwencji ucieczki (np. `\n` dla nowej linii).
- `-E`: Wyłącza interpretację sekwencji ucieczki (domyślne zachowanie).

## Common Examples
1. Wyświetlenie prostego tekstu:
   ```bash
   echo "Witaj, świecie!"
   ```

2. Wyświetlenie tekstu bez znaku nowej linii:
   ```bash
   echo -n "To jest bez nowej linii."
   ```

3. Użycie sekwencji ucieczki do wyświetlenia nowej linii:
   ```bash
   echo -e "Pierwsza linia\nDruga linia"
   ```

4. Wyświetlenie wartości zmiennej:
   ```bash
   imie="Jan"
   echo "Cześć, $imie!"
   ```

## Tips
- Używaj opcji `-n`, gdy chcesz kontynuować wyświetlanie tekstu w tej samej linii.
- Zawsze sprawdzaj, czy używasz odpowiednich sekwencji ucieczki z opcją `-e`, aby uzyskać oczekiwany format wyjściowy.
- `echo` jest przydatne w skryptach do debugowania, umożliwiając wyświetlanie wartości zmiennych w czasie wykonywania.