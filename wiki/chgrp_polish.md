# [Linux] C Shell (csh) chgrp: Zmiana grupy plików

## Overview
Polecenie `chgrp` służy do zmiany grupy przypisanej do plików lub katalogów w systemie Unix/Linux. Umożliwia to administratorom i użytkownikom zarządzanie dostępem do zasobów systemowych poprzez przypisywanie odpowiednich grup.

## Usage
Podstawowa składnia polecenia `chgrp` jest następująca:

```
chgrp [opcje] [argumenty]
```

## Common Options
- `-R`: Rekurencyjnie zmienia grupę dla katalogów i ich zawartości.
- `-v`: Wyświetla szczegóły dotyczące zmiany grupy dla każdego pliku.
- `-c`: Wyświetla tylko pliki, dla których zmiana grupy się powiodła.

## Common Examples
1. Zmiana grupy dla pojedynczego pliku:
   ```bash
   chgrp developers dokument.txt
   ```

2. Zmiana grupy dla katalogu:
   ```bash
   chgrp admin katalog/
   ```

3. Rekurencyjna zmiana grupy dla wszystkich plików w katalogu:
   ```bash
   chgrp -R users katalog/
   ```

4. Wyświetlenie szczegółów zmiany grupy:
   ```bash
   chgrp -v developers dokument.txt
   ```

5. Zmiana grupy tylko dla plików, które zostały zmienione:
   ```bash
   chgrp -c developers dokument.txt
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do zmiany grupy plików.
- Zawsze sprawdzaj aktualną grupę pliku przed dokonaniem zmian, używając polecenia `ls -l`.
- Używaj opcji `-R` ostrożnie, aby nie zmienić grupy dla niezamierzonych plików.