# [Linux] C Shell (csh) default użycie: Ustawienie domyślnej powłoki

## Overview
Polecenie `default` w C Shell (csh) służy do ustawiania domyślnej powłoki dla użytkownika w systemie. Umożliwia to skonfigurowanie, która powłoka będzie używana, gdy użytkownik loguje się do systemu.

## Usage
Podstawowa składnia polecenia `default` jest następująca:

```csh
default [options] [arguments]
```

## Common Options
- `-l`: Ustawia domyślną powłokę na powłokę logowania.
- `-s`: Ustawia domyślną powłokę na powłokę interaktywną.
- `-h`: Wyświetla pomoc dotycząca użycia polecenia.

## Common Examples
Przykłady użycia polecenia `default`:

1. Ustawienie domyślnej powłoki na powłokę logowania:
   ```csh
   default -l /bin/csh
   ```

2. Ustawienie domyślnej powłoki na powłokę interaktywną:
   ```csh
   default -s /bin/bash
   ```

3. Wyświetlenie pomocy dotyczącej polecenia:
   ```csh
   default -h
   ```

## Tips
- Upewnij się, że powłoka, którą chcesz ustawić jako domyślną, jest zainstalowana w systemie.
- Zawsze sprawdzaj, czy zmiany wprowadzone za pomocą polecenia `default` są zgodne z wymaganiami twojego środowiska pracy.
- Możesz użyć polecenia `echo $SHELL`, aby sprawdzić, która powłoka jest aktualnie ustawiona jako domyślna.