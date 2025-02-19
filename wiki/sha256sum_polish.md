# [Linux] C Shell (csh) sha256sum użycie: Obliczanie sum kontrolnych SHA-256

## Przegląd
Polecenie `sha256sum` służy do obliczania i weryfikowania sum kontrolnych SHA-256 dla plików. Jest to przydatne narzędzie do sprawdzania integralności danych oraz porównywania plików.

## Użycie
Podstawowa składnia polecenia `sha256sum` jest następująca:

```csh
sha256sum [opcje] [argumenty]
```

## Częste opcje
- `-b`: Oblicza sumę kontrolną dla plików binarnych.
- `-c`: Sprawdza sumy kontrolne z pliku.
- `-o <plik>`: Zapisuje wynik do określonego pliku.
- `--quiet`: Nie wyświetla komunikatów o błędach.

## Przykłady
1. Obliczanie sumy kontrolnej dla pliku:
   ```csh
   sha256sum plik.txt
   ```

2. Obliczanie sumy kontrolnej dla pliku binarnego:
   ```csh
   sha256sum -b plik.bin
   ```

3. Sprawdzanie sum kontrolnych z pliku:
   ```csh
   sha256sum -c suma.txt
   ```

4. Zapisanie sumy kontrolnej do pliku:
   ```csh
   sha256sum plik.txt -o wynik.txt
   ```

## Wskazówki
- Zawsze używaj opcji `-c`, aby upewnić się, że pliki nie zostały zmodyfikowane.
- Używaj plików z sumami kontrolnymi, aby łatwo weryfikować integralność danych w przyszłości.
- Pamiętaj, że suma kontrolna jest unikalna dla zawartości pliku, więc nawet najmniejsza zmiana w pliku spowoduje inną sumę kontrolną.