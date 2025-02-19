# [Linux] C Shell (csh) iconv użycie: Konwersja kodowania znaków

## Przegląd
Polecenie `iconv` służy do konwersji tekstu pomiędzy różnymi kodowaniami znaków. Jest to przydatne narzędzie, gdy potrzebujemy zmienić format pliku tekstowego, aby był zgodny z wymaganiami systemu lub aplikacji.

## Użycie
Podstawowa składnia polecenia `iconv` jest następująca:

```csh
iconv [opcje] [argumenty]
```

## Częste opcje
- `-f, --from-code=KOD`: Określa kodowanie źródłowe.
- `-t, --to-code=KOD`: Określa kodowanie docelowe.
- `-o, --output=PLIK`: Zapisuje wynik do określonego pliku.
- `-c`: Pomija nieprawidłowe znaki.

## Częste przykłady
1. Konwersja pliku z kodowania UTF-8 do ISO-8859-1:
   ```csh
   iconv -f UTF-8 -t ISO-8859-1 plik.txt -o plik_iso.txt
   ```

2. Wyświetlenie wyników konwersji na standardowe wyjście:
   ```csh
   iconv -f UTF-8 -t UTF-16 plik.txt
   ```

3. Pomijanie nieprawidłowych znaków podczas konwersji:
   ```csh
   iconv -f UTF-8 -t ASCII//TRANSLIT plik.txt -o plik_ascii.txt
   ```

## Wskazówki
- Zawsze sprawdzaj, jakie kodowanie jest używane w pliku źródłowym, aby uniknąć błędów konwersji.
- Używaj opcji `-o`, aby zapisać wynik do nowego pliku, co pozwoli uniknąć nadpisania oryginalnego pliku.
- Testuj konwersję na małych plikach, zanim zastosujesz ją do większych zbiorów danych.