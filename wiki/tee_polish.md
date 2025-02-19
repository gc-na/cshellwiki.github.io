# [Linux] C Shell (csh) tee użycie: Zapisz dane do pliku i wyświetl je na standardowym wyjściu

## Overview
Polecenie `tee` w powłoce C Shell (csh) służy do odczytywania danych ze standardowego wejścia i jednoczesnego zapisywania ich do jednego lub więcej plików. Umożliwia to użytkownikom monitorowanie danych w czasie rzeczywistym, podczas gdy są one zapisywane.

## Usage
Podstawowa składnia polecenia `tee` wygląda następująco:

```csh
tee [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `tee`:

- `-a`: Dodaje dane do istniejącego pliku zamiast go nadpisywać.
- `-i`: Ignoruje sygnał przerwania (SIGINT), co pozwala na kontynuowanie działania polecenia.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `tee`:

1. Zapisz dane do pliku i wyświetl je na ekranie:
   ```csh
   echo "Hello, World!" | tee output.txt
   ```

2. Dodaj dane do istniejącego pliku:
   ```csh
   echo "Nowa linia" | tee -a output.txt
   ```

3. Użyj `tee` z wieloma plikami:
   ```csh
   echo "Zapisz do dwóch plików" | tee file1.txt file2.txt
   ```

4. Ignoruj sygnał przerwania:
   ```csh
   some_command | tee -i output.txt
   ```

## Tips
- Używaj opcji `-a`, gdy chcesz dodać dane do pliku, aby uniknąć przypadkowego nadpisania.
- Możesz używać `tee` w połączeniu z innymi poleceniami, aby monitorować ich wyjście w czasie rzeczywistym.
- Pamiętaj, że `tee` działa najlepiej w skryptach lub w sytuacjach, gdzie potrzebujesz zarówno wyjścia na ekranie, jak i zapisu do pliku.