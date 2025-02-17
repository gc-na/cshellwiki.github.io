# [Linux] Bash nohup użycie: Uruchamianie procesów w tle

## Overview
Polecenie `nohup` (no hang up) pozwala na uruchamianie procesów w tle, które nie zostaną przerwane, nawet jeśli użytkownik wyloguje się z systemu. Jest to przydatne w sytuacjach, gdy chcesz, aby proces kontynuował działanie po zamknięciu terminala.

## Usage
Podstawowa składnia polecenia `nohup` jest następująca:

```bash
nohup [opcje] [argumenty]
```

## Common Options
- `&` - Uruchamia proces w tle.
- `-o [plik]` - Przekierowuje standardowe wyjście do określonego pliku.
- `-e [plik]` - Przekierowuje standardowe wyjście błędów do określonego pliku.

## Common Examples
1. Uruchamianie skryptu w tle:
   ```bash
   nohup ./myscript.sh &
   ```

2. Uruchamianie polecenia z przekierowaniem wyjścia do pliku:
   ```bash
   nohup mycommand > output.log &
   ```

3. Uruchamianie polecenia z przekierowaniem błędów:
   ```bash
   nohup mycommand 2> error.log &
   ```

4. Uruchamianie polecenia z przekierowaniem zarówno wyjścia, jak i błędów:
   ```bash
   nohup mycommand > output.log 2> error.log &
   ```

## Tips
- Zawsze używaj `&`, aby uruchomić proces w tle, co pozwoli na dalszą pracę w terminalu.
- Sprawdzaj pliki wyjściowe, aby monitorować postęp procesu.
- Używaj `disown`, aby odłączyć proces od terminala po jego uruchomieniu.