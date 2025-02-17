# [Linux] Bash exit użycie: Zakończenie skryptu lub sesji

## Overview
Polecenie `exit` w Bash służy do zakończenia bieżącego skryptu lub sesji powłoki. Można je wykorzystać do zwrócenia kodu zakończenia, który może być użyty przez inne skrypty lub programy do określenia, czy wykonanie zakończyło się powodzeniem, czy wystąpił błąd.

## Usage
Podstawowa składnia polecenia `exit` jest następująca:

```bash
exit [options] [status]
```

## Common Options
- `status`: Opcjonalny argument, który określa kod zakończenia. Domyślnie jest to 0, co oznacza, że skrypt zakończył się pomyślnie. Wartości różne od 0 wskazują na błędy.

## Common Examples

1. Zakończenie skryptu z domyślnym kodem zakończenia (0):
   ```bash
   #!/bin/bash
   echo "Zakończenie skryptu."
   exit
   ```

2. Zakończenie skryptu z określonym kodem zakończenia (np. 1):
   ```bash
   #!/bin/bash
   echo "Wystąpił błąd."
   exit 1
   ```

3. Użycie `exit` w interaktywnej sesji powłoki:
   ```bash
   exit
   ```

4. Zakończenie skryptu w zależności od warunku:
   ```bash
   #!/bin/bash
   if [ -f "plik.txt" ]; then
       echo "Plik istnieje."
       exit 0
   else
       echo "Plik nie istnieje."
       exit 1
   fi
   ```

## Tips
- Zawsze używaj odpowiednich kodów zakończenia, aby ułatwić debugowanie i zarządzanie błędami w skryptach.
- Możesz używać zmiennych do dynamicznego określania kodów zakończenia w skryptach.
- Pamiętaj, że `exit` kończy nie tylko skrypt, ale także sesję powłoki, jeśli jest używane w interaktywnej sesji.