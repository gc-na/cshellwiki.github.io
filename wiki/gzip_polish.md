# [Linux] Bash gzip użycie: Kompresja plików

## Overview
Polecenie `gzip` służy do kompresji plików, zmniejszając ich rozmiar, co ułatwia przechowywanie i przesyłanie danych. Gzip jest powszechnie używane w systemach Unix i Linux.

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

3. Kompresja pliku z zachowaniem oryginału:
   ```bash
   gzip -k plik.txt
   ```

4. Kompresja wszystkich plików w katalogu:
   ```bash
   gzip *.txt
   ```

5. Kompresja plików w podkatalogach:
   ```bash
   gzip -r katalog/
   ```

## Tips
- Używaj opcji `-v`, aby śledzić postęp kompresji i uzyskać informacje o rozmiarze plików.
- Pamiętaj, że po kompresji plików z rozszerzeniem `.gz`, oryginalne pliki zostaną usunięte, chyba że użyjesz opcji `-k`.
- Gzip jest bardziej efektywny w kompresji tekstu niż plików binarnych, dlatego warto go używać głównie do plików tekstowych.