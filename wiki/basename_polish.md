# [Linux] Bash basename użycie: Wyodrębnia nazwę pliku z pełnej ścieżki

## Overview
Polecenie `basename` służy do wyodrębniania nazwy pliku z pełnej ścieżki. Jest to przydatne, gdy chcemy uzyskać tylko nazwę pliku bez jego lokalizacji.

## Usage
Podstawowa składnia polecenia `basename` jest następująca:

```bash
basename [opcje] [argumenty]
```

## Common Options
- `-a`: Obsługuje wiele argumentów i zwraca nazwy plików dla każdego z nich.
- `-s SUFFIX`: Usuwa określony sufiks z nazwy pliku, jeśli jest obecny.

## Common Examples
1. Wyodrębnienie nazwy pliku z pełnej ścieżki:
   ```bash
   basename /home/użytkownik/dokumenty/plik.txt
   ```
   Wynik: `plik.txt`

2. Usunięcie sufiksu z nazwy pliku:
   ```bash
   basename /home/użytkownik/dokumenty/plik.txt .txt
   ```
   Wynik: `plik`

3. Obsługa wielu plików:
   ```bash
   basename -a /home/użytkownik/dokumenty/plik1.txt /home/użytkownik/dokumenty/plik2.txt
   ```
   Wynik:
   ```
   plik1.txt
   plik2.txt
   ```

4. Usunięcie sufiksu z wielu plików:
   ```bash
   basename -a /home/użytkownik/dokumenty/plik1.txt /home/użytkownik/dokumenty/plik2.txt .txt
   ```
   Wynik:
   ```
   plik1
   plik2
   ```

## Tips
- Używaj opcji `-s`, aby łatwo usunąć niepotrzebne sufiksy z nazw plików.
- Możesz łączyć `basename` z innymi poleceniami, takimi jak `find`, aby przetwarzać wiele plików w jednym kroku.
- Pamiętaj, że `basename` zwraca tylko nazwy plików, a nie ich lokalizacje, co może być przydatne w skryptach automatyzujących.