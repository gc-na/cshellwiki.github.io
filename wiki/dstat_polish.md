# [Linux] Bash dstat użycie: monitorowanie zasobów systemowych w czasie rzeczywistym

## Overview
Polecenie `dstat` jest narzędziem do monitorowania zasobów systemowych w czasie rzeczywistym. Umożliwia użytkownikom uzyskanie szczegółowych informacji o wydajności systemu, takich jak użycie CPU, pamięci, dysku, sieci i innych zasobów, co jest przydatne do analizy i diagnozowania problemów.

## Usage
Podstawowa składnia polecenia `dstat` jest następująca:

```bash
dstat [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `dstat`:

- `-c`: wyświetla użycie CPU.
- `-d`: pokazuje statystyki dysku.
- `-n`: monitoruje ruch sieciowy.
- `-m`: wyświetla użycie pamięci.
- `-t`: dodaje znacznik czasu do wyjścia.

## Common Examples
Oto kilka praktycznych przykładów użycia `dstat`:

1. Aby monitorować użycie CPU i pamięci:
   ```bash
   dstat -c -m
   ```

2. Aby uzyskać informacje o ruchu sieciowym i statystykach dysku:
   ```bash
   dstat -n -d
   ```

3. Aby monitorować wszystkie dostępne zasoby z czasem:
   ```bash
   dstat -tcdmn
   ```

4. Aby zapisać dane do pliku CSV:
   ```bash
   dstat --output statystyki.csv
   ```

## Tips
- Używaj opcji `-t`, aby dodać znaczniki czasu, co ułatwia analizę danych.
- Możesz łączyć różne opcje, aby uzyskać bardziej szczegółowe informacje w jednym widoku.
- Regularne monitorowanie zasobów systemowych może pomóc w identyfikacji wąskich gardeł i problemów z wydajnością.