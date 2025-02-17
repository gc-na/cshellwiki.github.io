# [Linux] Bash rsync użycie: Synchronizacja plików i katalogów

## Overview
Rsync to potężne narzędzie do synchronizacji plików i katalogów między różnymi lokalizacjami. Umożliwia efektywne przesyłanie danych, minimalizując ilość przesyłanych danych dzięki mechanizmowi różnicowemu.

## Usage
Podstawowa składnia polecenia rsync wygląda następująco:

```bash
rsync [opcje] [źródło] [cel]
```

## Common Options
- `-a`: Archiwizuje, co oznacza, że zachowuje uprawnienia, symlink, itp.
- `-v`: Włącza tryb szczegółowy, aby wyświetlić postęp operacji.
- `-z`: Kompresuje dane podczas przesyłania, co może przyspieszyć transfer.
- `-r`: Rekurencyjnie synchronizuje katalogi.
- `--delete`: Usuwa pliki w katalogu docelowym, które nie istnieją w katalogu źródłowym.

## Common Examples
1. Synchronizacja lokalnego katalogu z innym lokalnym katalogiem:
   ```bash
   rsync -av /ścieżka/do/katalogu1/ /ścieżka/do/katalogu2/
   ```

2. Synchronizacja lokalnego katalogu z katalogiem na zdalnym serwerze:
   ```bash
   rsync -av /ścieżka/do/katalogu/ użytkownik@serwer:/ścieżka/do/katalogu/
   ```

3. Synchronizacja z kompresją:
   ```bash
   rsync -avz /ścieżka/do/katalogu/ użytkownik@serwer:/ścieżka/do/katalogu/
   ```

4. Synchronizacja z usunięciem nieaktualnych plików:
   ```bash
   rsync -av --delete /ścieżka/do/katalogu1/ /ścieżka/do/katalogu2/
   ```

## Tips
- Zawsze testuj polecenie z opcją `-n` (symulacja), aby zobaczyć, co zostanie zrobione, zanim faktycznie wykonasz synchronizację.
- Używaj opcji `-e` do określenia protokołu SSH, jeśli synchronizujesz zdalnie, np. `rsync -av -e ssh /ścieżka/do/katalogu/ użytkownik@serwer:/ścieżka/do/katalogu/`.
- Regularnie twórz kopie zapasowe ważnych danych przed użyciem opcji `--delete`.