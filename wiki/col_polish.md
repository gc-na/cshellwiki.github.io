# [Linux] Bash col użycie: Usuwa kontrolki z tekstu

## Overview
Polecenie `col` jest używane do usuwania kontrolnych sekwencji z tekstu, co pozwala na poprawne wyświetlanie go w terminalu. Jest to przydatne, gdy chcemy przetworzyć tekst, który zawiera znaki kontrolne, takie jak kody formatujące.

## Usage
Podstawowa składnia polecenia `col` jest następująca:

```bash
col [opcje] [argumenty]
```

## Common Options
- `-b`: Ignoruje wszystkie sekwencje kontrolne, które są używane do formatowania tekstu.
- `-x`: Używa rozszerzonego formatu, co może być przydatne w przypadku bardziej złożonych dokumentów.
- `-f`: Zmienia wszystkie sekwencje kontrolne na odpowiednie znaki, co może być pomocne w niektórych sytuacjach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `col`:

1. Usuwanie sekwencji kontrolnych z pliku:
   ```bash
   col < plik_z_kontrolkami.txt > plik_bez_kontrolk.txt
   ```

2. Wyświetlanie tekstu bez kontrolnych sekwencji w terminalu:
   ```bash
   cat plik_z_kontrolkami.txt | col
   ```

3. Użycie opcji `-b` do ignorowania sekwencji kontrolnych:
   ```bash
   col -b < plik_z_kontrolkami.txt > plik_bez_kontrolk.txt
   ```

## Tips
- Używaj `col` w połączeniu z innymi poleceniami, takimi jak `cat` lub `less`, aby poprawić czytelność tekstu.
- Sprawdzaj zawartość plików przed i po użyciu `col`, aby upewnić się, że usunięcie sekwencji kontrolnych nie wpłynęło negatywnie na dane.
- Pamiętaj, że `col` działa najlepiej z plikami tekstowymi, które zawierają sekwencje kontrolne, więc nie zawsze będzie potrzebne w przypadku prostych plików tekstowych.