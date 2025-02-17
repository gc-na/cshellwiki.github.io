# [Linux] Bash stat użycie: Wyświetlanie informacji o plikach

## Overview
Polecenie `stat` w systemie Linux służy do wyświetlania szczegółowych informacji o plikach i katalogach. Umożliwia uzyskanie danych takich jak rozmiar pliku, daty modyfikacji, uprawnienia oraz inne atrybuty.

## Usage
Podstawowa składnia polecenia `stat` jest następująca:

```bash
stat [opcje] [argumenty]
```

## Common Options
- `-c, --format=FORMAT` - Umożliwia określenie formatu wyjścia.
- `-f, --file-system` - Wyświetla informacje o systemie plików, a nie o pliku.
- `--help` - Wyświetla pomoc dotyczącą polecenia.
- `--version` - Wyświetla wersję polecenia.

## Common Examples
1. Wyświetlenie podstawowych informacji o pliku:
   ```bash
   stat plik.txt
   ```

2. Wyświetlenie informacji o katalogu:
   ```bash
   stat /home/użytkownik
   ```

3. Użycie opcji formatu, aby wyświetlić tylko rozmiar pliku:
   ```bash
   stat -c %s plik.txt
   ```

4. Wyświetlenie informacji o systemie plików:
   ```bash
   stat -f /
   ```

## Tips
- Używaj opcji `-c` z odpowiednimi formatami, aby dostosować wyjście do swoich potrzeb.
- Możesz użyć `stat` w skryptach do automatycznego sprawdzania atrybutów plików.
- Pamiętaj, że `stat` może działać na wielu plikach jednocześnie, wystarczy podać je jako argumenty.