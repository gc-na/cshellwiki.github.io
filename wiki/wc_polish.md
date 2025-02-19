# [Linux] C Shell (csh) wc użycie: zliczanie linii, słów i bajtów

## Przegląd
Polecenie `wc` (word count) w C Shell służy do zliczania linii, słów i bajtów w plikach tekstowych. Jest to przydatne narzędzie do analizy zawartości plików.

## Użycie
Podstawowa składnia polecenia `wc` jest następująca:

```csh
wc [opcje] [argumenty]
```

## Często używane opcje
- `-l` – zlicza tylko linie.
- `-w` – zlicza tylko słowa.
- `-c` – zlicza tylko bajty.
- `-m` – zlicza znaki (w tym przypadku również znaki multibyte).

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `wc`:

1. Zliczanie linii w pliku:
   ```csh
   wc -l plik.txt
   ```

2. Zliczanie słów w pliku:
   ```csh
   wc -w plik.txt
   ```

3. Zliczanie bajtów w pliku:
   ```csh
   wc -c plik.txt
   ```

4. Zliczanie linii, słów i bajtów jednocześnie:
   ```csh
   wc plik.txt
   ```

5. Zliczanie linii w wielu plikach:
   ```csh
   wc -l plik1.txt plik2.txt
   ```

## Wskazówki
- Używaj opcji `-l`, `-w` i `-c` w zależności od tego, co chcesz zliczyć, aby uzyskać bardziej precyzyjne wyniki.
- Możesz używać `wc` w połączeniu z innymi poleceniami, na przykład z `grep`, aby zliczać linie spełniające określone kryteria:
  ```csh
  grep "szukany_tekst" plik.txt | wc -l
  ```
- Zawsze sprawdzaj, czy plik, który chcesz zliczyć, istnieje, aby uniknąć błędów.