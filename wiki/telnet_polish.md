# [Linux] Bash telnet użycie: Protokół komunikacyjny

## Overview
Polecenie `telnet` jest używane do nawiązywania połączeń zdalnych z serwerami za pomocą protokołu Telnet. Umożliwia użytkownikom interakcję z systemami zdalnymi, co jest przydatne w diagnostyce sieci oraz w zarządzaniu serwerami.

## Usage
Podstawowa składnia polecenia `telnet` jest następująca:

```bash
telnet [opcje] [adres] [port]
```

## Common Options
- `-l [nazwa_użytkownika]`: Umożliwia logowanie się jako określony użytkownik.
- `-d`: Włącza tryb debugowania, co może pomóc w diagnozowaniu problemów z połączeniem.
- `-n [plik]`: Umożliwia zapisanie sesji do określonego pliku.
- `-h`: Wyświetla pomoc i dostępne opcje.

## Common Examples
- Nawiązanie połączenia z serwerem na porcie 23 (domyślny port Telnet):
    ```bash
    telnet example.com 23
    ```

- Nawiązanie połączenia z serwerem na porcie 80 (HTTP):
    ```bash
    telnet example.com 80
    ```

- Logowanie się jako określony użytkownik:
    ```bash
    telnet -l user example.com
    ```

- Włączenie trybu debugowania:
    ```bash
    telnet -d example.com
    ```

## Tips
- Używaj `telnet` tylko w zaufanych sieciach, ponieważ przesyła dane w postaci niezaszyfrowanej.
- Zamiast `telnet`, rozważ użycie `ssh` dla bezpieczniejszych połączeń.
- Sprawdzaj dostępność portów na serwerze, aby upewnić się, że usługa jest uruchomiona przed próbą połączenia.