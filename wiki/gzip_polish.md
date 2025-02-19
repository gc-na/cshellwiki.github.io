# [Linux] C Shell (csh) gzip użycie: Kompresja plików

## Overview
Polecenie `gzip` służy do kompresji plików, zmniejszając ich rozmiar, co ułatwia przechowywanie i przesyłanie danych. Gzip jest popularnym narzędziem w systemach Unix i Linux, które wykorzystuje algorytm DEFLATE do efektywnej kompresji.

## Usage
Podstawowa składnia polecenia `gzip` jest następująca:

```bash
gzip [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `gzip`:

- `-d` lub `--decompress`: Dekompresuje plik.
- `-k` lub `--keep`: Zachowuje oryginalny plik po kompresji.
- `-v` lub `--verbose`: Wyświetla szczegółowe informacje o procesie kompresji.
- `-r` lub `--recursive`: Kompresuje pliki w podkatalogach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `gzip`:

1. Kompresja pliku:
   ```bash
   gzip plik.txt
   ```

2. Dekomprensja pliku:
   ```bash
   gzip -d plik.txt.gz
   ```

3. Kompresja z zachowaniem oryginalnego pliku:
   ```bash
   gzip -k plik.txt
   ```

4. Kompresja wszystkich plików `.txt` w katalogu:
   ```bash
   gzip *.txt
   ```

5. Kompresja plików w podkatalogach:
   ```bash
   gzip -r katalog/
   ```

## Tips
- Zawsze sprawdzaj rozmiar plików po kompresji, aby upewnić się, że proces był skuteczny.
- Używaj opcji `-v`, aby monitorować postęp kompresji i uzyskać informacje o rozmiarze plików przed i po.
- Pamiętaj, że pliki skompresowane za pomocą `gzip` mają rozszerzenie `.gz`, co ułatwia ich identyfikację.