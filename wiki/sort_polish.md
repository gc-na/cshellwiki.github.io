# [Linux] C Shell (csh) sort użycie: sortowanie danych

## Overview
Polecenie `sort` służy do sortowania linii tekstu w plikach lub z wejścia standardowego. Umożliwia uporządkowanie danych w różnych porządkach, co jest przydatne w analizie i przetwarzaniu informacji.

## Usage
Podstawowa składnia polecenia `sort` wygląda następująco:

```csh
sort [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `sort`:

- `-n`: Sortuje numerycznie.
- `-r`: Sortuje w odwrotnej kolejności.
- `-k`: Określa klucz sortowania (np. kolumnę).
- `-u`: Usuwa duplikaty po sortowaniu.
- `-o`: Zapisuje wynik sortowania do określonego pliku.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `sort`:

1. Sortowanie pliku tekstowego alfabetycznie:
   ```csh
   sort plik.txt
   ```

2. Sortowanie numeryczne:
   ```csh
   sort -n liczby.txt
   ```

3. Sortowanie w odwrotnej kolejności:
   ```csh
   sort -r plik.txt
   ```

4. Sortowanie według drugiej kolumny:
   ```csh
   sort -k 2 plik.txt
   ```

5. Zapisanie posortowanego wyniku do nowego pliku:
   ```csh
   sort plik.txt -o posortowany.txt
   ```

## Tips
- Używaj opcji `-u`, aby szybko usunąć duplikaty z wyników sortowania.
- Możesz łączyć różne opcje, na przykład `sort -n -r`, aby sortować numerycznie w odwrotnej kolejności.
- Zawsze sprawdzaj zawartość pliku wynikowego, aby upewnić się, że sortowanie przebiegło zgodnie z oczekiwaniami.