# [Linux] Bash find użycie: znajdowanie plików

## Overview
Polecenie `find` służy do przeszukiwania systemu plików w poszukiwaniu plików i katalogów, które spełniają określone kryteria. Umożliwia użytkownikom lokalizowanie plików na podstawie różnych atrybutów, takich jak nazwa, typ, rozmiar czy data modyfikacji.

## Usage
Podstawowa składnia polecenia `find` jest następująca:

```bash
find [ścieżka] [opcje] [argumenty]
```

## Common Options
- `-name [nazwa]`: wyszukuje pliki o podanej nazwie.
- `-type [typ]`: filtruje wyniki według typu pliku (np. `f` dla plików, `d` dla katalogów).
- `-size [rozmiar]`: znajduje pliki o określonym rozmiarze (np. `+100k` dla plików większych niż 100 KB).
- `-mtime [liczba]`: wyszukuje pliki zmodyfikowane w ciągu ostatnich `liczba` dni.
- `-exec [polecenie] {} \;`: wykonuje określone polecenie na każdym znalezionym pliku.

## Common Examples
- Znajdowanie plików o nazwie `example.txt` w bieżącym katalogu i podkatalogach:
  ```bash
  find . -name "example.txt"
  ```

- Wyszukiwanie wszystkich katalogów w systemie:
  ```bash
  find / -type d
  ```

- Znajdowanie plików większych niż 1 MB w katalogu domowym:
  ```bash
  find ~ -type f -size +1M
  ```

- Wyszukiwanie plików zmodyfikowanych w ciągu ostatnich 7 dni:
  ```bash
  find . -mtime -7
  ```

- Usuwanie wszystkich plików `.tmp` w katalogu tymczasowym:
  ```bash
  find /tmp -name "*.tmp" -exec rm {} \;
  ```

## Tips
- Używaj opcji `-type`, aby ograniczyć wyniki do określonego typu pliku, co przyspiesza wyszukiwanie.
- Zawsze testuj polecenia `-exec` z opcją `echo`, aby upewnić się, że wykonasz odpowiednie operacje na plikach.
- Możesz używać opcji `-print` (domyślnie włączona), aby wyświetlić wyniki wyszukiwania w czytelny sposób.