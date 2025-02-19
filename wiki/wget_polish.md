# [Linux] C Shell (csh) wget użycie: Pobieranie plików z internetu

## Overview
Polecenie `wget` jest narzędziem do pobierania plików z internetu. Obsługuje różne protokoły, takie jak HTTP, HTTPS i FTP, co czyni go wszechstronnym narzędziem do ściągania zawartości z sieci.

## Usage
Podstawowa składnia polecenia `wget` jest następująca:

```
wget [opcje] [argumenty]
```

## Common Options
- `-O [plik]`: Zapisuje pobrany plik pod określoną nazwą.
- `-c`: Wznawia przerwane pobieranie.
- `-q`: Włącza tryb cichy, minimalizując ilość wyświetlanych informacji.
- `--limit-rate=[prędkość]`: Ogranicza prędkość pobierania do określonej wartości.
- `-r`: Pobiera pliki rekurencyjnie, co oznacza, że ściąga również pliki z linków na stronie.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `wget`:

1. Pobieranie pojedynczego pliku:
   ```bash
   wget http://example.com/plik.txt
   ```

2. Zapisanie pliku pod inną nazwą:
   ```bash
   wget -O nowa_nazwa.txt http://example.com/plik.txt
   ```

3. Wznawianie przerwanego pobierania:
   ```bash
   wget -c http://example.com/plik.zip
   ```

4. Pobieranie plików rekurencyjnie:
   ```bash
   wget -r http://example.com/
   ```

5. Ograniczenie prędkości pobierania:
   ```bash
   wget --limit-rate=100k http://example.com/plik.zip
   ```

## Tips
- Używaj opcji `-q`, gdy chcesz pobierać pliki w tle bez zbędnych komunikatów.
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do pobierania plików z danej strony.
- Rozważ użycie opcji `-r` z `--no-parent`, aby uniknąć pobierania plików z wyższych katalogów.