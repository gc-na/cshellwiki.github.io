# [Linux] C Shell (csh) groupmod użycie: Modyfikacja grup użytkowników

## Overview
Polecenie `groupmod` służy do modyfikacji istniejących grup użytkowników w systemie. Umożliwia zmianę nazwy grupy oraz innych atrybutów, co jest przydatne w zarządzaniu uprawnieniami i organizacją użytkowników.

## Usage
Podstawowa składnia polecenia `groupmod` jest następująca:

```
groupmod [opcje] [argumenty]
```

## Common Options
- `-n, --new-name NEW_GROUP`: Zmienia nazwę grupy na `NEW_GROUP`.
- `-g, --gid GID`: Ustawia nowy identyfikator grupy (GID).
- `-o, --non-unique`: Pozwala na użycie GID, który nie jest unikalny.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `groupmod`:

1. Zmiana nazwy grupy:
   ```bash
   groupmod -n nowa_nazwa_starej_grupy stara_nazwa_grupy
   ```

2. Zmiana GID grupy:
   ```bash
   groupmod -g 1001 nazwa_grupy
   ```

3. Użycie GID, który nie jest unikalny:
   ```bash
   groupmod -o -g 1002 nazwa_grupy
   ```

## Tips
- Zawsze upewnij się, że nowa nazwa grupy nie koliduje z istniejącymi grupami w systemie.
- Przed dokonaniem zmian, warto wykonać kopię zapasową pliku `/etc/group`.
- Używaj polecenia `getent group` do sprawdzenia istniejących grup i ich GID przed modyfikacją.