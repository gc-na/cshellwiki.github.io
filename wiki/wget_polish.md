# [Linux] Bash wget użycie: Pobieranie plików z internetu

## Overview
Polecenie `wget` jest narzędziem wiersza poleceń, które umożliwia pobieranie plików z internetu. Obsługuje różne protokoły, takie jak HTTP, HTTPS i FTP, co czyni go wszechstronnym narzędziem do pobierania zasobów.

## Usage
Podstawowa składnia polecenia `wget` wygląda następująco:

```bash
wget [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `wget`:

- `-O <plik>`: Zapisuje pobrany plik pod określoną nazwą.
- `-c`: Wznawia przerwane pobieranie.
- `-q`: Włącza tryb cichy, nie wyświetlając postępu pobierania.
- `--limit-rate=<prędkość>`: Ogranicza prędkość pobierania do określonej wartości.
- `-r`: Włącza rekurencyjne pobieranie, co pozwala na pobieranie całych stron internetowych.

## Common Examples
Oto kilka praktycznych przykładów użycia `wget`:

1. **Pobieranie pojedynczego pliku:**
   ```bash
   wget https://example.com/plik.txt
   ```

2. **Pobieranie pliku i zapisanie go pod inną nazwą:**
   ```bash
   wget -O nowa_nazwa.txt https://example.com/plik.txt
   ```

3. **Wznawianie przerwanego pobierania:**
   ```bash
   wget -c https://example.com/plik.txt
   ```

4. **Pobieranie całej strony internetowej:**
   ```bash
   wget -r https://example.com
   ```

5. **Ograniczenie prędkości pobierania:**
   ```bash
   wget --limit-rate=200k https://example.com/plik.txt
   ```

## Tips
- Używaj opcji `-q`, gdy chcesz pobierać pliki w tle bez zbędnych informacji w terminalu.
- Jeśli pobierasz dużą stronę, rozważ użycie opcji `-r` z `--no-parent`, aby uniknąć pobierania plików z wyższych katalogów.
- Zawsze sprawdzaj, czy masz odpowiednie zezwolenia na pobieranie plików z danej strony, aby uniknąć naruszenia praw autorskich.