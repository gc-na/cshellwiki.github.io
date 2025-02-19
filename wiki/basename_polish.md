# [Linux] C Shell (csh) basename użycie: Usuwa ścieżki z nazw plików

## Overview
Polecenie `basename` w C Shell (csh) służy do usuwania ścieżek z nazw plików, zwracając jedynie nazwę pliku. Jest to przydatne, gdy chcemy uzyskać samą nazwę pliku bez jego lokalizacji w systemie plików.

## Usage
Podstawowa składnia polecenia `basename` jest następująca:

```csh
basename [opcje] [argumenty]
```

## Common Options
- `-a`: Obsługuje wiele argumentów i zwraca nazwę dla każdego z nich.
- `-s`: Umożliwia usunięcie określonego sufiksu z nazwy pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `basename`:

1. Uzyskanie nazwy pliku z pełnej ścieżki:
   ```csh
   basename /usr/local/bin/skrypt.sh
   ```
   Wynik: `skrypt.sh`

2. Usunięcie sufiksu z nazwy pliku:
   ```csh
   basename plik.txt .txt
   ```
   Wynik: `plik`

3. Obsługa wielu argumentów:
   ```csh
   basename -a /usr/bin/komenda1 /usr/bin/komenda2
   ```
   Wynik:
   ```
   komenda1
   komenda2
   ```

## Tips
- Używaj opcji `-s`, aby łatwo usunąć niechciane sufiksy z nazw plików.
- Możesz używać `basename` w skryptach, aby dynamicznie przetwarzać nazwy plików.
- Pamiętaj, że `basename` zwraca tylko ostatni element ścieżki, więc jeśli potrzebujesz pełnej ścieżki, użyj polecenia `dirname`.