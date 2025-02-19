# [Linux] C Shell (csh) cmp Użycie: Porównywanie plików

## Overview
Polecenie `cmp` służy do porównywania dwóch plików binarnych lub tekstowych w celu wykrycia różnic. Jeśli pliki są identyczne, `cmp` nie zwraca żadnego komunikatu, a jeśli różnią się, wskazuje pierwszą różnicę.

## Usage
Podstawowa składnia polecenia `cmp` jest następująca:

```
cmp [opcje] [argumenty]
```

## Common Options
- `-l`: Wyświetla numery bajtów, w których występują różnice, oraz różniące się wartości bajtów.
- `-s`: Porównuje pliki w trybie cichym, nie wyświetlając żadnych komunikatów, tylko zwraca kod wyjścia.
- `-i OFFSET`: Pomija pierwsze OFFSET bajtów w każdym z plików przed porównaniem.
- `-n LIMIT`: Porównuje tylko LIMIT bajtów z każdego pliku.

## Common Examples
1. Porównanie dwóch plików:
   ```bash
   cmp plik1.txt plik2.txt
   ```

2. Porównanie plików z wyświetleniem różnic:
   ```bash
   cmp -l plik1.bin plik2.bin
   ```

3. Ciche porównanie plików:
   ```bash
   cmp -s plik1.txt plik2.txt
   ```

4. Porównanie tylko pierwszych 100 bajtów:
   ```bash
   cmp -n 100 plik1.txt plik2.txt
   ```

## Tips
- Używaj opcji `-s`, gdy chcesz szybko sprawdzić, czy pliki są identyczne, bez zbędnych komunikatów.
- Opcja `-l` jest przydatna, gdy potrzebujesz szczegółowych informacji o różnicach między plikami.
- Pamiętaj, że `cmp` porównuje pliki bajt po bajcie, więc nawet najmniejsza różnica zostanie zauważona.