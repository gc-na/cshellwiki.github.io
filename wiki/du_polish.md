# [Linux] Bash du użycie: Sprawdza rozmiar plików i katalogów

## Overview
Polecenie `du` (disk usage) służy do oceny rozmiaru plików i katalogów w systemie plików. Umożliwia użytkownikom monitorowanie zajętości dysku i identyfikowanie dużych plików lub katalogów, które mogą zajmować cenne miejsce.

## Usage
Podstawowa składnia polecenia `du` wygląda następująco:

```bash
du [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `du`:

- `-h` : Wyświetla rozmiary w formacie czytelnym dla ludzi (np. KB, MB).
- `-s` : Wyświetla tylko całkowity rozmiar dla każdego argumentu, bez szczegółów.
- `-a` : Wyświetla rozmiary wszystkich plików, a nie tylko katalogów.
- `-c` : Podsumowuje całkowity rozmiar dla wszystkich argumentów.
- `--max-depth=N` : Ogranicza głębokość wyświetlania katalogów do N.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `du`:

1. Sprawdzenie rozmiaru bieżącego katalogu:

   ```bash
   du -h
   ```

2. Wyświetlenie całkowitego rozmiaru katalogu:

   ```bash
   du -sh /ścieżka/do/katalogu
   ```

3. Wyświetlenie rozmiaru wszystkich plików i katalogów w bieżącym katalogu:

   ```bash
   du -ah
   ```

4. Ograniczenie wyświetlania do głębokości 1:

   ```bash
   du -h --max-depth=1
   ```

5. Podsumowanie całkowitego rozmiaru kilku katalogów:

   ```bash
   du -ch /ścieżka/do/katalogu1 /ścieżka/do/katalogu2
   ```

## Tips
- Używaj opcji `-h`, aby uzyskać bardziej zrozumiałe wyniki, zwłaszcza gdy pracujesz z dużymi plikami.
- Regularnie monitoruj rozmiar katalogów, aby uniknąć problemów z brakiem miejsca na dysku.
- Możesz użyć `du` w połączeniu z innymi poleceniami, takimi jak `sort`, aby znaleźć największe pliki lub katalogi:

   ```bash
   du -ah | sort -rh | head -n 10
   ```

Dzięki tym wskazówkom i przykładom, możesz skutecznie korzystać z polecenia `du` do zarządzania przestrzenią dyskową w swoim systemie.