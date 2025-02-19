# [Linux] C Shell (csh) find użycie: znajdowanie nazw plików

## Przegląd
Polecenie `find` w C Shell (csh) służy do wyszukiwania plików i katalogów w hierarchii systemu plików na podstawie określonych kryteriów, takich jak nazwa, typ, rozmiar czy data modyfikacji.

## Użycie
Podstawowa składnia polecenia `find` jest następująca:

```csh
find [opcje] [argumenty]
```

## Częste opcje
- `-name <nazwa>`: wyszukuje pliki o podanej nazwie.
- `-type <typ>`: filtruje wyniki według typu pliku (np. `f` dla plików, `d` dla katalogów).
- `-size <rozmiar>`: wyszukuje pliki o określonym rozmiarze.
- `-mtime <liczba>`: wyszukuje pliki zmodyfikowane w ciągu ostatnich `liczba` dni.
- `-exec <polecenie> {} \;`: wykonuje podane polecenie na każdym znalezionym pliku.

## Częste przykłady
- Znajdowanie plików o nazwie `plik.txt` w bieżącym katalogu i podkatalogach:

```csh
find . -name "plik.txt"
```

- Wyszukiwanie wszystkich katalogów w systemie:

```csh
find / -type d
```

- Znajdowanie plików większych niż 1 MB:

```csh
find . -size +1M
```

- Wyszukiwanie plików zmodyfikowanych w ciągu ostatnich 7 dni:

```csh
find . -mtime -7
```

- Usuwanie wszystkich plików z rozszerzeniem `.tmp`:

```csh
find . -name "*.tmp" -exec rm {} \;
```

## Wskazówki
- Używaj opcji `-print` (domyślnie włączona w wielu systemach), aby wyświetlić wyniki wyszukiwania.
- Zawsze testuj polecenia `find` z opcją `-print` przed użyciem `-exec`, aby upewnić się, że operujesz na właściwych plikach.
- Możesz używać opcji `-maxdepth` i `-mindepth`, aby ograniczyć głębokość przeszukiwania katalogów, co może przyspieszyć proces.