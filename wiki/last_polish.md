# [Linux] Bash last użycie: wyświetlanie ostatnich logowań użytkowników

## Overview
Polecenie `last` służy do wyświetlania listy ostatnich logowań użytkowników w systemie. Informacje te są pobierane z pliku `/var/log/wtmp`, który rejestruje wszystkie logowania i wylogowania.

## Usage
Podstawowa składnia polecenia `last` jest następująca:

```bash
last [opcje] [argumenty]
```

## Common Options
- `-a`: Wyświetla adresy IP zdalnych hostów.
- `-n [liczba]`: Określa liczbę ostatnich logowań do wyświetlenia.
- `-R`: Nie wyświetla nagłówka z nazwą hosta.
- `-x`: Wyświetla również informacje o rebootach i shutdownach systemu.

## Common Examples
1. Wyświetlenie wszystkich ostatnich logowań:
   ```bash
   last
   ```

2. Wyświetlenie ostatnich 5 logowań:
   ```bash
   last -n 5
   ```

3. Wyświetlenie logowań z adresami IP:
   ```bash
   last -a
   ```

4. Wyświetlenie logowań oraz rebootów:
   ```bash
   last -x
   ```

5. Wyświetlenie logowań dla konkretnego użytkownika:
   ```bash
   last username
   ```

## Tips
- Używaj opcji `-n`, aby ograniczyć liczbę wyświetlanych logowań do bardziej przystępnej ilości.
- Regularnie sprawdzaj logi, aby monitorować aktywność użytkowników w systemie.
- Możesz użyć polecenia `lastb`, aby sprawdzić nieudane próby logowania, co może pomóc w identyfikacji potencjalnych zagrożeń bezpieczeństwa.