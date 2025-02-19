# [Linux] C Shell (csh) last: wyświetlanie ostatnich logowań użytkowników

## Overview
Polecenie `last` w C Shell (csh) służy do wyświetlania listy ostatnich logowań użytkowników w systemie. Informacje te są pobierane z pliku `/var/log/wtmp`, który rejestruje wszystkie logowania i wylogowania.

## Usage
Podstawowa składnia polecenia `last` jest następująca:

```
last [opcje] [argumenty]
```

## Common Options
- `-n [liczba]`: Wyświetla określoną liczbę ostatnich logowań.
- `-R`: Ukrywa nazwę hosta w wynikach.
- `-f [plik]`: Używa innego pliku niż domyślny `/var/log/wtmp`.

## Common Examples
1. Wyświetlenie wszystkich ostatnich logowań:
   ```csh
   last
   ```

2. Wyświetlenie ostatnich 10 logowań:
   ```csh
   last -n 10
   ```

3. Wyświetlenie logowań z ukrytymi nazwami hostów:
   ```csh
   last -R
   ```

4. Użycie innego pliku do wyświetlenia logowań:
   ```csh
   last -f /path/to/your/logfile
   ```

## Tips
- Regularnie sprawdzaj logi, aby monitorować aktywność użytkowników w systemie.
- Używaj opcji `-n`, aby ograniczyć wyniki do najbardziej istotnych logowań.
- Pamiętaj, że dostęp do pliku `/var/log/wtmp` może wymagać uprawnień administratora.