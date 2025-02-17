# [Linux] Bash sha512sum użycie: Obliczanie sum kontrolnych SHA-512

## Overview
Polecenie `sha512sum` służy do obliczania i weryfikacji sum kontrolnych plików przy użyciu algorytmu SHA-512. Jest to przydatne narzędzie do zapewnienia integralności danych, umożliwiające sprawdzenie, czy plik nie został zmodyfikowany.

## Usage
Podstawowa składnia polecenia `sha512sum` jest następująca:

```bash
sha512sum [opcje] [argumenty]
```

## Common Options
- `-b`, `--binary` - Oblicza sumę kontrolną w trybie binarnym.
- `-c`, `--check` - Sprawdza sumy kontrolne z pliku.
- `-h`, `--help` - Wyświetla pomoc dotycząca polecenia.
- `-o`, `--output=FILE` - Zapisuje wynik do określonego pliku.

## Common Examples
1. Obliczanie sumy kontrolnej dla pliku:
   ```bash
   sha512sum plik.txt
   ```

2. Zapisanie sumy kontrolnej do pliku:
   ```bash
   sha512sum plik.txt > suma.txt
   ```

3. Sprawdzanie sum kontrolnych z pliku:
   ```bash
   sha512sum -c suma.txt
   ```

4. Obliczanie sumy kontrolnej w trybie binarnym:
   ```bash
   sha512sum -b plik.bin
   ```

## Tips
- Zawsze zapisuj sumy kontrolne w osobnym pliku, aby móc je później wykorzystać do weryfikacji.
- Używaj opcji `-c`, aby łatwo sprawdzić integralność wielu plików jednocześnie.
- Regularnie sprawdzaj sumy kontrolne pobranych plików, aby upewnić się, że nie zostały one uszkodzone lub zmodyfikowane.