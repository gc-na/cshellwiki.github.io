# [Linux] Bash id użycie: wyświetlanie informacji o użytkowniku

## Overview
Polecenie `id` w systemie Linux służy do wyświetlania informacji o użytkowniku, w tym identyfikatora użytkownika (UID), identyfikatora grupy (GID) oraz przynależności do grup. Jest to przydatne narzędzie do zarządzania użytkownikami i grupami w systemie.

## Usage
Podstawowa składnia polecenia `id` jest następująca:

```bash
id [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `id`:

- `-u`: Wyświetla tylko identyfikator użytkownika (UID).
- `-g`: Wyświetla tylko identyfikator grupy (GID).
- `-G`: Wyświetla wszystkie identyfikatory grup, do których należy użytkownik.
- `-n`: Wyświetla nazwy zamiast identyfikatorów (w połączeniu z `-u`, `-g` lub `-G`).

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `id`:

1. Wyświetlenie pełnych informacji o bieżącym użytkowniku:

   ```bash
   id
   ```

2. Wyświetlenie tylko identyfikatora użytkownika (UID):

   ```bash
   id -u
   ```

3. Wyświetlenie tylko identyfikatora grupy (GID):

   ```bash
   id -g
   ```

4. Wyświetlenie wszystkich identyfikatorów grup, do których należy użytkownik:

   ```bash
   id -G
   ```

5. Wyświetlenie nazwy bieżącego użytkownika:

   ```bash
   id -un
   ```

## Tips
- Użyj opcji `-n`, aby uzyskać bardziej czytelne wyniki, zwłaszcza gdy pracujesz z identyfikatorami grup.
- Możesz podać nazwę użytkownika jako argument, aby uzyskać informacje o innym użytkowniku, na przykład:

  ```bash
  id username
  ```

- Regularne sprawdzanie informacji o użytkownikach i grupach może pomóc w zarządzaniu uprawnieniami w systemie.