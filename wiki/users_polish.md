# [Linux] Użytkownicy C Shell (csh): Wyświetlanie aktywnych użytkowników

## Overview
Polecenie `users` w powłoce C Shell (csh) służy do wyświetlania nazw użytkowników, którzy są aktualnie zalogowani na systemie. Jest to przydatne narzędzie do szybkiego sprawdzenia, kto jest aktywny w danym momencie.

## Usage
Podstawowa składnia polecenia `users` jest następująca:

```
users [options] [arguments]
```

## Common Options
- `-n`: Wyświetla liczbę unikalnych użytkowników.
- `-l`: Wyświetla pełne imiona użytkowników (jeśli dostępne).

## Common Examples
1. Wyświetlenie wszystkich zalogowanych użytkowników:
   ```csh
   users
   ```

2. Wyświetlenie liczby unikalnych użytkowników:
   ```csh
   users -n
   ```

3. Wyświetlenie pełnych imion użytkowników:
   ```csh
   users -l
   ```

## Tips
- Użyj polecenia `who` lub `w`, jeśli potrzebujesz bardziej szczegółowych informacji o zalogowanych użytkownikach, takich jak czas logowania czy aktywność.
- Polecenie `users` jest szybkie i efektywne, ale nie pokazuje szczegółowych informacji, więc warto łączyć je z innymi poleceniami dla lepszego obrazu sytuacji w systemie.