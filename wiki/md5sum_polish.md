# [Linux] Bash md5sum użycie: Obliczanie sum kontrolnych MD5

## Przegląd
Polecenie `md5sum` służy do obliczania i weryfikacji sum kontrolnych MD5 dla plików. Jest to przydatne narzędzie do sprawdzania integralności danych, umożliwiające wykrycie zmian w plikach.

## Użycie
Podstawowa składnia polecenia `md5sum` jest następująca:

```bash
md5sum [opcje] [argumenty]
```

## Często używane opcje
- `-b`: Oblicza sumę kontrolną dla plików binarnych.
- `-c`: Sprawdza sumy kontrolne z pliku.
- `-t`: Oblicza sumę kontrolną dla danych z standardowego wejścia.
- `--help`: Wyświetla pomoc dotyczącą użycia polecenia.

## Przykłady
1. **Obliczanie sumy kontrolnej dla pliku:**

   ```bash
   md5sum plik.txt
   ```

2. **Zapis sum kontrolnych do pliku:**

   ```bash
   md5sum plik1.txt plik2.txt > sumy.txt
   ```

3. **Weryfikacja sum kontrolnych z pliku:**

   ```bash
   md5sum -c sumy.txt
   ```

4. **Obliczanie sumy kontrolnej dla danych z wejścia:**

   ```bash
   echo "Przykładowy tekst" | md5sum
   ```

## Wskazówki
- Używaj opcji `-b`, gdy pracujesz z plikami binarnymi, aby uzyskać dokładne wyniki.
- Zawsze zapisuj sumy kontrolne w osobnym pliku, aby móc je później łatwo zweryfikować.
- Regularnie sprawdzaj integralność ważnych plików, aby upewnić się, że nie zostały one zmienione.