# [Linux] C Shell (csh) nohup użycie: Uruchamianie procesów w tle

## Przegląd
Polecenie `nohup` (no hang up) w systemie C Shell (csh) służy do uruchamiania procesów w tle, które nie zostaną przerwane, nawet jeśli użytkownik wyloguje się z sesji. Dzięki temu można kontynuować wykonywanie długotrwałych zadań bez obawy o ich zakończenie.

## Użycie
Podstawowa składnia polecenia `nohup` jest następująca:

```
nohup [opcje] [argumenty]
```

## Często używane opcje
- `&` - uruchamia proces w tle.
- `-o [plik]` - przekierowuje standardowe wyjście do określonego pliku.
- `-e [plik]` - przekierowuje standardowe wyjście błędów do określonego pliku.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `nohup`:

1. Uruchomienie skryptu w tle:
   ```csh
   nohup ./myscript.sh &
   ```

2. Uruchomienie polecenia `ping` w tle i zapisanie wyjścia do pliku:
   ```csh
   nohup ping google.com > ping_output.txt &
   ```

3. Uruchomienie procesu z przekierowaniem błędów do innego pliku:
   ```csh
   nohup ./myapp 2> error_log.txt &
   ```

4. Uruchomienie długotrwałego zadania i zapisanie zarówno wyjścia, jak i błędów:
   ```csh
   nohup ./long_running_task > output.log 2>&1 &
   ```

## Wskazówki
- Zawsze używaj `&` na końcu polecenia, aby uruchomić proces w tle.
- Sprawdzaj pliki wyjściowe, aby monitorować postęp zadań uruchomionych za pomocą `nohup`.
- Używaj opcji przekierowania, aby lepiej zarządzać wyjściem i błędami, co ułatwia debugowanie.