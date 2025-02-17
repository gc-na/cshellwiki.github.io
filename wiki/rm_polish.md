# [Linux] Bash rm użycie: Usuwanie plików i katalogów

## Overview
Polecenie `rm` w systemie Linux służy do usuwania plików i katalogów. Jest to potężne narzędzie, które pozwala na szybkie pozbycie się niepotrzebnych danych z systemu.

## Usage
Podstawowa składnia polecenia `rm` wygląda następująco:

```
rm [opcje] [argumenty]
```

## Common Options
- `-f` : Wymusza usunięcie plików bez pytania o potwierdzenie.
- `-i` : Pyta o potwierdzenie przed usunięciem każdego pliku.
- `-r` : Usuwa katalogi oraz ich zawartość rekurencyjnie.
- `-v` : Wyświetla szczegóły dotyczące usuwanych plików.

## Common Examples
1. Usunięcie pojedynczego pliku:
   ```bash
   rm plik.txt
   ```

2. Usunięcie wielu plików:
   ```bash
   rm plik1.txt plik2.txt plik3.txt
   ```

3. Usunięcie katalogu i jego zawartości:
   ```bash
   rm -r katalog/
   ```

4. Wymuszenie usunięcia pliku bez potwierdzenia:
   ```bash
   rm -f plik.txt
   ```

5. Usunięcie pliku z potwierdzeniem:
   ```bash
   rm -i plik.txt
   ```

## Tips
- Zawsze sprawdzaj, co usuwasz, aby uniknąć przypadkowego usunięcia ważnych plików.
- Używaj opcji `-i`, aby mieć dodatkową warstwę bezpieczeństwa, szczególnie przy usuwaniu wielu plików.
- Rozważ użycie polecenia `mv` do przenoszenia plików do kosza zamiast ich bezpośredniego usuwania, co pozwala na ich późniejsze odzyskanie.