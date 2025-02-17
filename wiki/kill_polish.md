# [Linux] Bash kill użycie: Zakończ procesy

## Overview
Polecenie `kill` w systemie Linux służy do wysyłania sygnałów do procesów, co najczęściej wykorzystywane jest do ich zakończenia. Dzięki temu użytkownicy mogą zarządzać działającymi aplikacjami i procesami w systemie.

## Usage
Podstawowa składnia polecenia `kill` wygląda następująco:

```bash
kill [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `kill`:

- `-l`: Wyświetla listę dostępnych sygnałów.
- `-s SIGNAL`: Określa sygnał do wysłania (domyślnie jest to `TERM`).
- `-n NUMBER`: Wysyła sygnał o numerze podanym w argumentach.
- `-p`: Wysyła sygnał do procesów, które są potomkami bieżącego procesu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `kill`:

1. Zakończenie procesu za pomocą jego PID (identyfikatora procesu):

   ```bash
   kill 1234
   ```

2. Wysłanie sygnału `SIGKILL` (natychmiastowe zakończenie procesu):

   ```bash
   kill -9 1234
   ```

3. Wysłanie sygnału `SIGTERM` do wielu procesów:

   ```bash
   kill 1234 5678 91011
   ```

4. Wyświetlenie listy dostępnych sygnałów:

   ```bash
   kill -l
   ```

5. Zakończenie procesu na podstawie nazwy (używając `pkill`):

   ```bash
   pkill nazwa_procesu
   ```

## Tips
- Zawsze staraj się używać sygnału `SIGTERM` (domyślnie) przed `SIGKILL`, ponieważ pozwala to procesowi na prawidłowe zakończenie.
- Używaj `ps` lub `top`, aby znaleźć PID procesów, które chcesz zakończyć.
- Pamiętaj, że do zakończenia niektórych procesów mogą być wymagane uprawnienia administratora, więc w razie potrzeby użyj `sudo`.