# [Linux] C Shell (csh) gunzip użycie: Rozpakowywanie plików gzip

## Przegląd
Polecenie `gunzip` służy do dekompresji plików skompresowanych za pomocą algorytmu gzip. Umożliwia użytkownikom łatwe przywracanie oryginalnych plików z formatu skompresowanego.

## Użycie
Podstawowa składnia polecenia `gunzip` jest następująca:

```
gunzip [opcje] [argumenty]
```

## Częste opcje
- `-c`: Wyświetla dekompresowane dane na standardowym wyjściu, zamiast zapisywać je w pliku.
- `-f`: Wymusza dekompresję, nawet jeśli plik docelowy już istnieje.
- `-k`: Zachowuje oryginalny plik skompresowany po dekompresji.
- `-r`: Rekursywnie dekompresuje wszystkie pliki w podkatalogach.

## Częste przykłady
1. Aby dekompresować pojedynczy plik:
   ```bash
   gunzip plik.gz
   ```

2. Aby dekompresować plik i zachować oryginał:
   ```bash
   gunzip -k plik.gz
   ```

3. Aby dekompresować wszystkie pliki `.gz` w bieżącym katalogu:
   ```bash
   gunzip *.gz
   ```

4. Aby dekompresować plik i wyświetlić wynik na standardowym wyjściu:
   ```bash
   gunzip -c plik.gz
   ```

5. Aby dekompresować plik w podkatalogach:
   ```bash
   gunzip -r katalog/
   ```

## Wskazówki
- Upewnij się, że masz odpowiednie uprawnienia do zapisu w katalogu, w którym chcesz dekompresować pliki.
- Zawsze sprawdzaj, czy plik `.gz` jest poprawny przed próbą dekompresji, aby uniknąć błędów.
- Używaj opcji `-k`, jeśli chcesz zachować oryginalny plik skompresowany na wypadek, gdybyś potrzebował go ponownie.