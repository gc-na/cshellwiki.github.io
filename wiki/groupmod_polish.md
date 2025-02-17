# [Linux] Bash groupmod użycie: Zmiana właściwości grupy

## Overview
Polecenie `groupmod` służy do modyfikacji istniejących grup w systemie Linux. Umożliwia administratorom systemu zmianę różnych właściwości grup, takich jak nazwa grupy czy identyfikator grupy (GID).

## Usage
Podstawowa składnia polecenia `groupmod` wygląda następująco:

```bash
groupmod [opcje] [argumenty]
```

## Common Options
- `-n, --new-name NEW_NAME`: Zmienia nazwę grupy na `NEW_NAME`.
- `-g, --gid GID`: Ustawia nowy identyfikator grupy (GID).
- `-o`: Pozwala na użycie GID, który już jest przypisany do innej grupy (domyślnie nie jest to dozwolone).

## Common Examples
1. Zmiana nazwy grupy:
   ```bash
   groupmod -n nowa_nazwa_starej_grupy stara_nazwa_grupy
   ```

2. Zmiana GID grupy:
   ```bash
   groupmod -g 1001 nazwa_grupy
   ```

3. Zmiana nazwy grupy i GID jednocześnie:
   ```bash
   groupmod -n nowa_nazwa -g 1002 nazwa_grupy
   ```

## Tips
- Zawsze sprawdzaj, czy nowa nazwa grupy lub GID nie koliduje z istniejącymi grupami w systemie.
- Używaj polecenia `getent group` do wyświetlenia listy grup i ich GID przed dokonaniem zmian.
- Pamiętaj, że zmiana GID może wpłynąć na uprawnienia do plików i katalogów przypisanych do tej grupy.