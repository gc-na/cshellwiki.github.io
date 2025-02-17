# [Linux] Bash sha256sum użycie: Oblicza sumę kontrolną SHA-256 plików

## Overview
Polecenie `sha256sum` służy do obliczania sumy kontrolnej SHA-256 dla plików. Jest to przydatne narzędzie do weryfikacji integralności danych, umożliwiające sprawdzenie, czy plik nie został zmodyfikowany.

## Usage
Podstawowa składnia polecenia `sha256sum` wygląda następująco:

```bash
sha256sum [opcje] [argumenty]
```

## Common Options
- `-b` : Oblicza sumę kontrolną dla plików binarnych.
- `-c` : Sprawdza sumy kontrolne z pliku.
- `-o <plik>` : Zapisuje wynik do określonego pliku.
- `--quiet` : Nie wyświetla komunikatów o błędach.

## Common Examples
1. Obliczanie sumy kontrolnej dla pojedynczego pliku:
   ```bash
   sha256sum plik.txt
   ```

2. Obliczanie sumy kontrolnej dla wielu plików:
   ```bash
   sha256sum plik1.txt plik2.txt
   ```

3. Zapisanie sumy kontrolnej do pliku:
   ```bash
   sha256sum plik.txt > suma.txt
   ```

4. Sprawdzanie sum kontrolnych z pliku:
   ```bash
   sha256sum -c suma.txt
   ```

5. Obliczanie sumy kontrolnej dla pliku binarnego:
   ```bash
   sha256sum -b plik.bin
   ```

## Tips
- Używaj opcji `-c`, aby szybko zweryfikować integralność plików na podstawie wcześniej obliczonych sum kontrolnych.
- Zapisuj sumy kontrolne w plikach, aby móc je łatwo sprawdzić w przyszłości.
- Pamiętaj, że zmiana jakiejkolwiek części pliku spowoduje zmianę jego sumy kontrolnej, co jest kluczowe dla weryfikacji integralności.