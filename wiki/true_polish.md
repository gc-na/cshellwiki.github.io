# [Linux] Bash true użycie: Zwraca prawdę

## Overview
Polecenie `true` w systemie Linux jest prostym narzędziem, które zawsze zwraca kod wyjścia 0, co oznacza sukces. Jest często używane w skryptach i automatyzacji, gdzie potrzebne jest potwierdzenie, że operacja zakończyła się pomyślnie.

## Usage
Podstawowa składnia polecenia `true` jest następująca:

```bash
true [opcje] [argumenty]
```

## Common Options
Polecenie `true` nie ma żadnych opcji ani argumentów, które by zmieniały jego działanie. Zawsze zwraca ten sam wynik.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `true`:

1. **Sprawdzenie, czy polecenie zakończyło się sukcesem:**
   ```bash
   if true; then
       echo "To polecenie zakończyło się sukcesem!"
   fi
   ```

2. **Użycie w skrypcie do testowania:**
   ```bash
   #!/bin/bash
   true
   echo "Skrypt zakończony pomyślnie."
   ```

3. **Wykorzystanie w pętli:**
   ```bash
   while true; do
       echo "Ta pętla będzie działać w nieskończoność."
       break  # Użycie break, aby przerwać pętlę
   done
   ```

## Tips
- Używaj `true` w skryptach, aby zapewnić, że pewne sekcje kodu są zawsze wykonywane.
- Możesz użyć `true` w połączeniu z innymi poleceniami, aby stworzyć bardziej złożone logiki warunkowe.
- `true` jest bardzo szybkie i nie wymaga żadnych zasobów, co czyni je idealnym do testowania i debugowania.