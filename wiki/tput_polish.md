# [Linux] Bash tput użycie: Zmiana atrybutów terminala

## Overview
Polecenie `tput` służy do interakcji z terminalem, umożliwiając użytkownikom kontrolowanie atrybutów wyświetlania, takich jak kolory tekstu, pozycjonowanie kursora czy czyszczenie ekranu. Dzięki `tput` można dostosować wygląd i zachowanie terminala w skryptach Bash.

## Usage
Podstawowa składnia polecenia `tput` jest następująca:

```bash
tput [opcje] [argumenty]
```

## Common Options
- `setaf [n]` - Ustawia kolor tekstu na kolor o numerze `n`.
- `setab [n]` - Ustawia kolor tła na kolor o numerze `n`.
- `clear` - Czyści ekran terminala.
- `cup [x] [y]` - Ustawia kursor w pozycji (x, y).
- `bold` - Ustawia tekst na pogrubiony.

## Common Examples
1. Ustawienie koloru tekstu na czerwony:
   ```bash
   tput setaf 1
   echo "To jest czerwony tekst"
   ```

2. Ustawienie koloru tła na niebieski:
   ```bash
   tput setab 4
   echo "To jest tekst na niebieskim tle"
   ```

3. Czyszczenie ekranu:
   ```bash
   tput clear
   ```

4. Ustawienie kursora w pozycji (10, 5):
   ```bash
   tput cup 10 5
   echo "Kursor jest tutaj"
   ```

5. Ustawienie tekstu na pogrubiony:
   ```bash
   tput bold
   echo "To jest pogrubiony tekst"
   ```

## Tips
- Używaj `tput reset`, aby przywrócić domyślne ustawienia terminala po zakończeniu skryptu.
- Możesz łączyć różne atrybuty, np. ustawić kolor i pogrubienie w jednym poleceniu.
- Sprawdź dostępne kolory i ich numery, aby lepiej dostosować wyświetlanie tekstu w terminalu.