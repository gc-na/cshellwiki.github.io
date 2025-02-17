# [Linux] Bash cmp użycie: Porównywanie plików

## Overview
Polecenie `cmp` służy do porównywania dwóch plików w celu określenia, czy są one identyczne. Jeśli pliki różnią się, `cmp` wskazuje pierwszą różnicę, co czyni je przydatnym narzędziem do wykrywania zmian w plikach.

## Usage
Podstawowa składnia polecenia `cmp` jest następująca:

```bash
cmp [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `cmp`:

- `-l`: Wyświetla numery bajtów, w których występują różnice, oraz różnice w postaci wartości szesnastkowych.
- `-s`: Porównuje pliki, ale nie wyświetla żadnych informacji. Zwraca tylko kod wyjścia.
- `-i OFFSET`: Pomija pierwsze `OFFSET` bajtów w każdym z plików przed porównaniem.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `cmp`:

1. Porównanie dwóch plików:
   ```bash
   cmp plik1.txt plik2.txt
   ```

2. Porównanie dwóch plików z wyświetleniem różnic w formacie szesnastkowym:
   ```bash
   cmp -l plik1.txt plik2.txt
   ```

3. Porównanie dwóch plików bez wyświetlania informacji:
   ```bash
   cmp -s plik1.txt plik2.txt
   ```

4. Porównanie plików, pomijając pierwsze 10 bajtów:
   ```bash
   cmp -i 10 plik1.txt plik2.txt
   ```

## Tips
- Użyj opcji `-s`, gdy chcesz szybko sprawdzić, czy pliki są identyczne, bez zbędnych informacji.
- Jeśli porównujesz duże pliki, rozważ użycie opcji `-l`, aby uzyskać szczegółowe informacje o różnicach.
- Pamiętaj, że `cmp` porównuje pliki bajt po bajcie, więc nawet najmniejsza różnica zostanie wykryta.