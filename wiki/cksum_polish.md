# [Linux] Bash cksum użycie: obliczanie sum kontrolnych plików

## Przegląd
Polecenie `cksum` służy do obliczania sum kontrolnych plików oraz ich rozmiarów w bajtach. Umożliwia to weryfikację integralności danych, co jest przydatne przy porównywaniu plików lub sprawdzaniu, czy plik nie został uszkodzony.

## Użycie
Podstawowa składnia polecenia `cksum` jest następująca:

```bash
cksum [opcje] [argumenty]
```

## Częste opcje
- `-a, --algorithm=ALGORYTM` - określa algorytm do obliczania sumy kontrolnej (np. md5, sha256).
- `-h, --help` - wyświetla pomoc dotyczącą użycia polecenia.
- `-V, --version` - wyświetla wersję programu.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `cksum`:

1. Oblicz sumę kontrolną dla pojedynczego pliku:
   ```bash
   cksum plik.txt
   ```

2. Oblicz sumę kontrolną dla wielu plików:
   ```bash
   cksum plik1.txt plik2.txt plik3.txt
   ```

3. Zapisz wynik do pliku:
   ```bash
   cksum plik.txt > suma.txt
   ```

4. Użyj opcji do wyświetlenia wersji:
   ```bash
   cksum -V
   ```

## Wskazówki
- Używaj `cksum` w połączeniu z innymi poleceniami, takimi jak `diff`, aby porównać sumy kontrolne dwóch plików.
- Regularnie obliczaj sumy kontrolne ważnych plików, aby upewnić się, że nie zostały one zmodyfikowane lub uszkodzone.
- Zapisuj sumy kontrolne w plikach tekstowych, aby móc je łatwo porównywać w przyszłości.