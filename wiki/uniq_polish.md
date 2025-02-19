# [Linux] C Shell (csh) uniq <Użycie: Usuwa duplikaty z pliku lub strumienia danych>

## Overview
Polecenie `uniq` służy do usuwania duplikatów z plików tekstowych lub strumieni danych. Działa na podstawie porównania sąsiadujących linii, co oznacza, że tylko powtarzające się linie obok siebie są eliminowane.

## Usage
Podstawowa składnia polecenia `uniq` jest następująca:

```
uniq [opcje] [argumenty]
```

## Common Options
- `-c`: Zlicza wystąpienia każdej unikalnej linii i wyświetla je przed linią.
- `-d`: Wyświetla tylko linie, które są duplikatami.
- `-u`: Wyświetla tylko linie, które są unikalne (niepowtarzające się).
- `-i`: Ignoruje wielkość liter podczas porównywania linii.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `uniq`:

1. Usunięcie duplikatów z pliku:
   ```csh
   uniq plik.txt
   ```

2. Zliczenie wystąpień unikalnych linii:
   ```csh
   uniq -c plik.txt
   ```

3. Wyświetlenie tylko duplikatów:
   ```csh
   uniq -d plik.txt
   ```

4. Ignorowanie wielkości liter:
   ```csh
   uniq -i plik.txt
   ```

5. Usunięcie duplikatów z wyjścia innego polecenia:
   ```csh
   sort plik.txt | uniq
   ```

## Tips
- Upewnij się, że plik jest posortowany przed użyciem `uniq`, aby wszystkie duplikaty były obok siebie.
- Możesz używać `uniq` w połączeniu z innymi poleceniami, takimi jak `sort`, aby uzyskać bardziej złożone wyniki.
- Zawsze sprawdzaj, czy chcesz usunąć wszystkie duplikaty, czy tylko niektóre, używając odpowiednich opcji.