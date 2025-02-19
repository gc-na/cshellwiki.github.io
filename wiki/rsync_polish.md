# [Linux] C Shell (csh) rsync użycie: Synchronizacja plików i katalogów

## Overview
Rsync to potężne narzędzie do synchronizacji plików i katalogów między lokalnym a zdalnym systemem. Umożliwia efektywne przesyłanie danych, minimalizując ilość przesyłanych informacji poprzez kopiowanie tylko zmienionych fragmentów plików.

## Usage
Podstawowa składnia polecenia rsync jest następująca:

```bash
rsync [options] [arguments]
```

## Common Options
- `-a`: Archiwizuje pliki, zachowując ich uprawnienia, daty modyfikacji i inne atrybuty.
- `-v`: Włącza tryb szczegółowy, wyświetlając postęp operacji.
- `-z`: Kompresuje dane podczas przesyłania, co może przyspieszyć transfer.
- `-r`: Rekurencyjnie synchronizuje katalogi.
- `--delete`: Usuwa pliki w docelowym katalogu, które nie istnieją w źródłowym.

## Common Examples
- Synchronizacja lokalnego katalogu do zdalnego serwera:
  ```bash
  rsync -av /local/directory/ user@remote:/remote/directory/
  ```

- Synchronizacja zdalnego katalogu do lokalnego:
  ```bash
  rsync -av user@remote:/remote/directory/ /local/directory/
  ```

- Synchronizacja z kompresją:
  ```bash
  rsync -avz /local/directory/ user@remote:/remote/directory/
  ```

- Synchronizacja z usunięciem niepotrzebnych plików:
  ```bash
  rsync -av --delete /local/directory/ user@remote:/remote/directory/
  ```

## Tips
- Zawsze testuj polecenie rsync z opcją `-n` (dry run), aby zobaczyć, co zostanie zrobione, zanim wykonasz rzeczywistą synchronizację.
- Używaj opcji `-e` do określenia protokołu SSH, jeśli chcesz zabezpieczyć transfer:
  ```bash
  rsync -av -e ssh /local/directory/ user@remote:/remote/directory/
  ```
- Regularnie twórz kopie zapasowe ważnych danych, korzystając z rsync, aby zapewnić ich bezpieczeństwo.