# [Linux] C Shell (csh) xz użycie: kompresja i dekompresja plików

## Przegląd
Polecenie `xz` służy do kompresji i dekompresji plików, wykorzystując algorytm LZMA. Jest to narzędzie, które pozwala na zmniejszenie rozmiaru plików, co jest szczególnie przydatne w przypadku dużych zbiorów danych.

## Użycie
Podstawowa składnia polecenia `xz` jest następująca:

```csh
xz [opcje] [argumenty]
```

## Częste opcje
- `-d`, `--decompress`: dekompresuje plik.
- `-k`, `--keep`: zachowuje oryginalny plik po kompresji.
- `-f`, `--force`: wymusza nadpisanie istniejących plików.
- `-z`, `--compress`: kompresuje plik (domyślna opcja).
- `-9`: używa maksymalnego poziomu kompresji.

## Przykłady
- Kompresja pliku:
```csh
xz myfile.txt
```

- Dekomprensja pliku:
```csh
xz -d myfile.txt.xz
```

- Kompresja z zachowaniem oryginalnego pliku:
```csh
xz -k myfile.txt
```

- Wymuszenie kompresji, nawet jeśli plik już istnieje:
```csh
xz -f myfile.txt
```

- Kompresja z maksymalnym poziomem:
```csh
xz -9 myfile.txt
```

## Wskazówki
- Używaj opcji `-k`, jeśli chcesz zachować oryginalne pliki podczas kompresji.
- Zwróć uwagę na rozmiar plików po kompresji; `xz` może znacznie zmniejszyć ich rozmiar, ale czasami może to zająć więcej czasu.
- Sprawdzaj dokumentację, aby poznać więcej opcji i dostosować kompresję do swoich potrzeb.