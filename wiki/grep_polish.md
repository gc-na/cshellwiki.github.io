# [Linux] C Shell (csh) grep Użycie: Wyszukiwanie wzorców w plikach

## Overview
Polecenie `grep` służy do wyszukiwania wzorców w plikach tekstowych. Umożliwia użytkownikom filtrowanie danych, aby znaleźć linie, które pasują do określonego wyrażenia regularnego.

## Usage
Podstawowa składnia polecenia `grep` wygląda następująco:

```csh
grep [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `grep`:

- `-i`: Ignoruje wielkość liter podczas wyszukiwania.
- `-v`: Zwraca linie, które **nie** pasują do wzorca.
- `-r`: Rekurencyjnie przeszukuje katalogi.
- `-n`: Wyświetla numery linii, w których znaleziono pasujące wzorce.
- `-l`: Zwraca tylko nazwy plików, które zawierają pasujące linie.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `grep`:

1. Wyszukiwanie wzorca w pliku:
   ```csh
   grep "wzorzec" plik.txt
   ```

2. Wyszukiwanie wzorca bez uwzględniania wielkości liter:
   ```csh
   grep -i "wzorzec" plik.txt
   ```

3. Wyszukiwanie wzorca w wielu plikach:
   ```csh
   grep "wzorzec" *.txt
   ```

4. Rekurencyjne przeszukiwanie katalogu:
   ```csh
   grep -r "wzorzec" /ścieżka/do/katalogu
   ```

5. Wyświetlanie numerów linii z pasującymi wzorcami:
   ```csh
   grep -n "wzorzec" plik.txt
   ```

## Tips
- Używaj opcji `-i`, gdy nie chcesz, aby wielkość liter wpływała na wyniki wyszukiwania.
- Aby szybko znaleźć pliki, które nie zawierają określonego wzorca, użyj opcji `-v`.
- W przypadku dużych katalogów, opcja `-r` może znacznie ułatwić przeszukiwanie.
- Zawsze sprawdzaj dokumentację (`man grep`), aby poznać więcej opcji i możliwości.