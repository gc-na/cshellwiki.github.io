# [Linux] C Shell (csh) sha512sum użycie: Obliczanie sum kontrolnych SHA-512

## Przegląd
Polecenie `sha512sum` służy do obliczania i weryfikacji sum kontrolnych SHA-512 dla plików. Jest to przydatne narzędzie do zapewnienia integralności danych, umożliwiające sprawdzenie, czy plik nie został zmodyfikowany.

## Użycie
Podstawowa składnia polecenia `sha512sum` jest następująca:

```csh
sha512sum [opcje] [argumenty]
```

## Częste opcje
- `-b` - Oblicza sumę kontrolną w trybie binarnym.
- `-c` - Sprawdza sumy kontrolne z pliku.
- `-h` - Wyświetla pomoc i informacje o użyciu.
- `--tag` - Dodaje znacznik do sumy kontrolnej.

## Przykłady
1. Obliczanie sumy kontrolnej dla pliku:
   ```csh
   sha512sum plik.txt
   ```

2. Zapisanie sumy kontrolnej do pliku:
   ```csh
   sha512sum plik.txt > suma.txt
   ```

3. Weryfikacja sum kontrolnych z pliku:
   ```csh
   sha512sum -c suma.txt
   ```

4. Obliczanie sumy kontrolnej w trybie binarnym:
   ```csh
   sha512sum -b plik.bin
   ```

## Wskazówki
- Zawsze zapisuj sumy kontrolne w osobnym pliku, aby móc je łatwo weryfikować w przyszłości.
- Używaj opcji `-c`, aby szybko sprawdzić integralność wielu plików naraz.
- Regularnie sprawdzaj sumy kontrolne ważnych plików, aby upewnić się, że nie zostały one zmodyfikowane.