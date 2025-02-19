# [Linux] C Shell (csh) at: Planowanie zadań do wykonania w przyszłości

## Overview
Polecenie `at` w systemie C Shell (csh) służy do planowania zadań, które mają być wykonane w określonym czasie w przyszłości. Umożliwia użytkownikom uruchamianie poleceń lub skryptów w wyznaczonym momencie, co jest przydatne w automatyzacji zadań.

## Usage
Podstawowa składnia polecenia `at` jest następująca:

```
at [opcje] [argumenty]
```

## Common Options
- `-f FILE`: Wczytuje polecenia do wykonania z pliku zamiast z standardowego wejścia.
- `-m`: Wysyła wiadomość e-mail po zakończeniu zadania, nawet jeśli nie wystąpiły żadne błędy.
- `-q QUEUE`: Umożliwia określenie kolejki, w której zadanie ma być wykonane.
- `-l`: Wyświetla listę zaplanowanych zadań.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `at`:

1. **Zaplanowanie prostego polecenia:**
   Aby zaplanować uruchomienie polecenia `echo` o godzinie 15:00, użyj:
   ```bash
   echo "echo 'Cześć, to jest zaplanowane zadanie!'" | at 15:00
   ```

2. **Zaplanowanie skryptu:**
   Aby uruchomić skrypt `backup.sh` o godzinie 2:00 w nocy:
   ```bash
   at 02:00 -f backup.sh
   ```

3. **Zaplanowanie zadania na jutro:**
   Aby zaplanować polecenie na jutro o 10:30:
   ```bash
   echo "rm -rf /tmp/*" | at 10:30 tomorrow
   ```

4. **Wyświetlenie zaplanowanych zadań:**
   Aby zobaczyć listę wszystkich zaplanowanych zadań:
   ```bash
   at -l
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do uruchamiania zaplanowanych zadań.
- Zawsze testuj swoje skrypty przed zaplanowaniem ich wykonania, aby uniknąć niepożądanych skutków.
- Możesz używać `atq` do przeglądania zaplanowanych zadań i `atrm` do ich usuwania.