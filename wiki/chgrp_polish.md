# [Linux] Bash chgrp użycie: Zmiana grupy plików

## Overview
Polecenie `chgrp` służy do zmiany grupy przypisanej do plików i katalogów w systemie Linux. Umożliwia to administratorom i użytkownikom zarządzanie dostępem do zasobów w systemie plików.

## Usage
Podstawowa składnia polecenia `chgrp` jest następująca:

```bash
chgrp [opcje] [argumenty]
```

## Common Options
- `-R` : Zmiana grupy rekurencyjnie dla wszystkich plików i katalogów w podanym katalogu.
- `-v` : Wyświetlenie informacji o tym, które pliki zostały zmienione.
- `-c` : Wyświetlenie informacji tylko o plikach, dla których zmiana grupy się powiodła.

## Common Examples
1. Zmiana grupy pliku:
   ```bash
   chgrp developers plik.txt
   ```

2. Zmiana grupy dla katalogu i wszystkich jego zawartości:
   ```bash
   chgrp -R developers katalog/
   ```

3. Wyświetlenie informacji o zmianach:
   ```bash
   chgrp -v developers plik.txt
   ```

4. Zmiana grupy dla wielu plików jednocześnie:
   ```bash
   chgrp developers plik1.txt plik2.txt plik3.txt
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do zmiany grupy plików.
- Zawsze używaj opcji `-v` lub `-c`, aby mieć pewność, że zmiany zostały zastosowane.
- Zmiana grupy rekurencyjnie (`-R`) może być przydatna, ale używaj jej ostrożnie, aby nie zmienić grupy plików, których nie chcesz modyfikować.