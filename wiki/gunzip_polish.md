# [Linux] Bash gunzip użycie: Rozpakowywanie plików gzip

## Overview
Polecenie `gunzip` jest używane do dekompresji plików skompresowanych za pomocą algorytmu gzip. Umożliwia ono przywrócenie oryginalnych plików z formatu .gz.

## Usage
Podstawowa składnia polecenia `gunzip` wygląda następująco:

```bash
gunzip [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `gunzip`:

- `-c`: Wyjście na standardowe wyjście (stdout) zamiast nadpisywania pliku.
- `-f`: Wymusza dekompresję, nawet jeśli plik docelowy już istnieje.
- `-k`: Zachowuje oryginalny plik skompresowany po dekompresji.
- `-r`: Rekursywnie dekompresuje wszystkie pliki w podkatalogach.

## Common Examples
Oto kilka praktycznych przykładów użycia `gunzip`:

1. **Dekomprensja pojedynczego pliku:**
   ```bash
   gunzip plik.gz
   ```

2. **Dekomprensja z zachowaniem oryginalnego pliku:**
   ```bash
   gunzip -k plik.gz
   ```

3. **Dekomprensja i wyświetlenie na standardowym wyjściu:**
   ```bash
   gunzip -c plik.gz > nowy_plik
   ```

4. **Dekomprensja wszystkich plików .gz w katalogu:**
   ```bash
   gunzip *.gz
   ```

5. **Rekurencyjna dekompresja plików w katalogu i podkatalogach:**
   ```bash
   gunzip -r katalog/
   ```

## Tips
- Zawsze upewnij się, że masz kopię zapasową ważnych plików przed dekompresją, zwłaszcza gdy używasz opcji `-f`.
- Użyj opcji `-k`, jeśli chcesz zachować skompresowany plik po dekompresji.
- Możesz użyć `zcat` jako alternatywy dla `gunzip -c`, aby wyświetlić zawartość skompresowanego pliku bez dekompresji do pliku.