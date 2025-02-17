# [Linux] Bash cp użycie: Kopiowanie plików i katalogów

## Overview
Polecenie `cp` w systemie Linux służy do kopiowania plików i katalogów. Umożliwia tworzenie kopii zapasowych lub przenoszenie danych w obrębie systemu plików.

## Usage
Podstawowa składnia polecenia `cp` jest następująca:

```bash
cp [opcje] [argumenty]
```

## Common Options
- `-r` lub `--recursive`: Kopiuje katalogi rekurencyjnie.
- `-i` lub `--interactive`: Pyta o potwierdzenie przed nadpisaniem istniejących plików.
- `-u` lub `--update`: Kopiuje tylko pliki, które są nowsze od istniejących lub które nie istnieją w katalogu docelowym.
- `-v` lub `--verbose`: Wyświetla szczegółowe informacje o kopiowanych plikach.

## Common Examples
1. **Kopiowanie pliku:**
   ```bash
   cp plik.txt kopia_plik.txt
   ```

2. **Kopiowanie katalogu rekurencyjnie:**
   ```bash
   cp -r katalog/ kopia_katalogu/
   ```

3. **Kopiowanie z potwierdzeniem:**
   ```bash
   cp -i plik.txt kopia_plik.txt
   ```

4. **Kopiowanie tylko nowszych plików:**
   ```bash
   cp -u plik.txt katalog/
   ```

5. **Kopiowanie z wyświetlaniem szczegółów:**
   ```bash
   cp -v plik.txt kopia_plik.txt
   ```

## Tips
- Zawsze używaj opcji `-i`, gdy kopiujesz pliki do katalogu, w którym mogą już istnieć pliki o tej samej nazwie, aby uniknąć przypadkowego nadpisania.
- Używaj opcji `-r` tylko wtedy, gdy chcesz skopiować całe katalogi, aby uniknąć błędów przy kopiowaniu plików.
- Regularnie twórz kopie zapasowe ważnych plików, aby zabezpieczyć się przed ich utratą.