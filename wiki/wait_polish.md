# [Linux] Bash wait użycie: Czekanie na zakończenie procesów

## Overview
Polecenie `wait` w Bash służy do czekania na zakończenie jednego lub więcej procesów. Umożliwia synchronizację skryptów, zapewniając, że dalsze instrukcje nie będą wykonywane, dopóki określone procesy nie zakończą swojego działania.

## Usage
Podstawowa składnia polecenia `wait` jest następująca:

```bash
wait [options] [arguments]
```

## Common Options
- `-n`: Czeka na zakończenie dowolnego procesu, a nie tylko na te, które zostały uruchomione w bieżącym skrypcie.
- `PID`: Można podać identyfikator procesu (PID), aby czekać tylko na zakończenie konkretnego procesu.

## Common Examples

### Czekanie na zakończenie wszystkich procesów
Aby poczekać na zakończenie wszystkich procesów uruchomionych w bieżącym skrypcie, użyj polecenia `wait` bez żadnych argumentów:

```bash
#!/bin/bash
sleep 5 &
sleep 3 &
wait
echo "Wszystkie procesy zakończone."
```

### Czekanie na konkretny proces
Możesz czekać na zakończenie konkretnego procesu, podając jego PID:

```bash
#!/bin/bash
sleep 5 &
PID=$!
echo "Czekam na proces o PID: $PID"
wait $PID
echo "Proces o PID: $PID zakończony."
```

### Czekanie na dowolny proces
Używając opcji `-n`, możesz czekać na zakończenie dowolnego procesu:

```bash
#!/bin/bash
sleep 5 &
sleep 3 &
wait -n
echo "Jeden z procesów zakończony."
```

## Tips
- Używaj `wait` w skryptach, aby zapewnić, że wszystkie procesy zakończą się przed kontynuowaniem dalszych działań.
- Zawsze sprawdzaj PID procesów, aby upewnić się, że czekasz na właściwe procesy.
- Możesz użyć `wait` w połączeniu z innymi poleceniami, aby tworzyć bardziej złożone skrypty, które wymagają synchronizacji.