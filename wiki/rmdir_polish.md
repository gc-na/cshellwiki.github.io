# [Linux] Bash rmdir użycie: Usuwanie pustych katalogów

## Overview
Polecenie `rmdir` służy do usuwania pustych katalogów w systemie Linux. Jeśli katalog zawiera jakiekolwiek pliki lub inne katalogi, `rmdir` nie będzie w stanie go usunąć.

## Usage
Podstawowa składnia polecenia `rmdir` jest następująca:

```bash
rmdir [opcje] [argumenty]
```

## Common Options
- `--ignore-fail-on-non-empty`: Ignoruje błędy, jeśli katalog nie jest pusty.
- `--verbose`: Wyświetla szczegółowe informacje o usuwanych katalogach.
- `--help`: Wyświetla pomoc dotyczącą polecenia.

## Common Examples
1. Usunięcie pustego katalogu:
   ```bash
   rmdir moj_katalog
   ```

2. Usunięcie wielu pustych katalogów jednocześnie:
   ```bash
   rmdir katalog1 katalog2 katalog3
   ```

3. Użycie opcji `--verbose` do uzyskania informacji o usuwanych katalogach:
   ```bash
   rmdir --verbose moj_katalog
   ```

4. Ignorowanie błędów przy próbie usunięcia niepustego katalogu:
   ```bash
   rmdir --ignore-fail-on-non-empty moj_katalog
   ```

## Tips
- Zawsze upewnij się, że katalog jest pusty przed użyciem `rmdir`, aby uniknąć błędów.
- Możesz użyć polecenia `ls` przed `rmdir`, aby sprawdzić zawartość katalogu.
- Jeśli chcesz usunąć katalog wraz z jego zawartością, rozważ użycie polecenia `rm -r` zamiast `rmdir`.