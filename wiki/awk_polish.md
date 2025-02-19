# [Linux] C Shell (csh) awk użycie: Przetwarzanie tekstu i danych

## Overview
Polecenie `awk` jest potężnym narzędziem do przetwarzania tekstu i danych w systemach Unix i Linux. Umożliwia analizowanie i przetwarzanie danych w formacie tekstowym, co czyni je idealnym do pracy z plikami tekstowymi oraz danymi w formacie CSV.

## Usage
Podstawowa składnia polecenia `awk` wygląda następująco:

```csh
awk [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji `awk`:

- `-F` - Ustawia separator pól, domyślnie jest to spacja.
- `-v` - Umożliwia przekazywanie zmiennych do skryptu `awk`.
- `-f` - Umożliwia wczytanie skryptu `awk` z pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia `awk`:

1. **Wyświetlenie drugiego pola z pliku:**
   ```csh
   awk '{print $2}' plik.txt
   ```

2. **Użycie innego separatora (np. przecinek):**
   ```csh
   awk -F, '{print $1}' plik.csv
   ```

3. **Zliczanie linii w pliku:**
   ```csh
   awk 'END {print NR}' plik.txt
   ```

4. **Filtracja wierszy na podstawie warunku:**
   ```csh
   awk '$3 > 50 {print $1, $2}' plik.txt
   ```

5. **Przekazywanie zmiennej do skryptu:**
   ```csh
   awk -v prog=100 '$3 > prog {print $1}' plik.txt
   ```

## Tips
- Używaj opcji `-F`, aby dostosować separator pól do formatu danych, z którym pracujesz.
- Zawsze testuj swoje skrypty `awk` na małych próbkach danych, aby upewnić się, że działają zgodnie z oczekiwaniami.
- Wykorzystuj zmienne do przechowywania wartości, które mogą być używane w różnych częściach skryptu, co zwiększa jego czytelność i elastyczność.