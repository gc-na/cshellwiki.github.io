# [Linux] C Shell (csh) du użycie: Sprawdza rozmiar katalogów i plików

## Overview
Polecenie `du` (disk usage) służy do wyświetlania rozmiaru plików i katalogów w systemie plików. Umożliwia użytkownikom zrozumienie, ile miejsca zajmują różne elementy na dysku.

## Usage
Podstawowa składnia polecenia `du` jest następująca:

```csh
du [opcje] [argumenty]
```

## Common Options
- `-h`: Wyświetla rozmiary w formacie czytelnym dla ludzi (np. KB, MB).
- `-s`: Podsumowuje rozmiar dla każdego argumentu, zamiast wyświetlać rozmiary dla wszystkich podkatalogów.
- `-a`: Wyświetla rozmiary dla wszystkich plików, nie tylko dla katalogów.
- `-c`: Dodaje podsumowanie całkowitego rozmiaru na końcu wyników.

## Common Examples
- Aby wyświetlić rozmiar katalogu w formacie czytelnym dla ludzi:
```csh
du -h /ścieżka/do/katalogu
```

- Aby uzyskać podsumowanie rozmiaru katalogu:
```csh
du -sh /ścieżka/do/katalogu
```

- Aby wyświetlić rozmiary wszystkich plików i katalogów w bieżącym katalogu:
```csh
du -ah .
```

- Aby uzyskać całkowity rozmiar wszystkich plików i katalogów w bieżącym katalogu:
```csh
du -ch .
```

## Tips
- Używaj opcji `-h`, aby łatwiej interpretować wyniki, zwłaszcza w przypadku dużych rozmiarów.
- Opcja `-s` jest przydatna, gdy chcesz szybko uzyskać ogólny obraz zajętości miejsca bez szczegółowego przeglądania.
- Regularne monitorowanie rozmiaru katalogów może pomóc w zarządzaniu przestrzenią dyskową i unikaniu problemów z brakiem miejsca.