# [Linux] C Shell (csh) bzip2 Użycie: Kompresja plików

## Przegląd
Polecenie `bzip2` służy do kompresji plików, zmniejszając ich rozmiar, co ułatwia przechowywanie i przesyłanie danych. Używa algorytmu Burrows-Wheeler, który zapewnia wysoką efektywność kompresji.

## Użycie
Podstawowa składnia polecenia `bzip2` jest następująca:

```csh
bzip2 [opcje] [argumenty]
```

## Często używane opcje
- `-d`, `--decompress`: Dekompresuje plik.
- `-k`, `--keep`: Zachowuje oryginalny plik po kompresji.
- `-f`, `--force`: Wymusza nadpisanie istniejących plików.
- `-v`, `--verbose`: Wyświetla szczegółowe informacje o procesie kompresji.

## Przykłady
1. Kompresja pliku:
   ```csh
   bzip2 plik.txt
   ```

2. Dekompresja pliku:
   ```csh
   bzip2 -d plik.txt.bz2
   ```

3. Kompresja z zachowaniem oryginalnego pliku:
   ```csh
   bzip2 -k plik.txt
   ```

4. Wymuszenie nadpisania istniejącego pliku:
   ```csh
   bzip2 -f plik.txt
   ```

5. Kompresja z wyświetlaniem szczegółowych informacji:
   ```csh
   bzip2 -v plik.txt
   ```

## Wskazówki
- Zawsze sprawdzaj, czy masz kopię zapasową ważnych plików przed ich kompresją.
- Używaj opcji `-k`, jeśli chcesz zachować oryginalne pliki.
- Pamiętaj, że pliki skompresowane za pomocą `bzip2` mają rozszerzenie `.bz2`.