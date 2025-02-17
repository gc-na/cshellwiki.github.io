# [Linux] Bash w at: Planowanie zadań do wykonania w przyszłości

## Overview
Polecenie `at` w systemie Linux służy do planowania jednorazowych zadań, które mają zostać wykonane w określonym czasie w przyszłości. Umożliwia użytkownikom uruchamianie poleceń lub skryptów o wyznaczonej porze, co jest przydatne w automatyzacji zadań.

## Usage
Podstawowa składnia polecenia `at` wygląda następująco:

```bash
at [opcje] [argumenty]
```

## Common Options
- `-f FILE` – Wykonaj polecenia z pliku zamiast z standardowego wejścia.
- `-m` – Wyślij e-mail po zakończeniu zadania, nawet jeśli nie wystąpiły żadne błędy.
- `-q QUEUE` – Określa kolejkę, w której zadanie ma być wykonane.
- `-l` – Wyświetla listę zaplanowanych zadań.
- `-d JOB_ID` – Usuwa zaplanowane zadanie o podanym identyfikatorze.

## Common Examples

1. **Zaplanowanie prostego zadania**
   Aby zaplanować polecenie `echo` na jutro o 10:00, użyj:
   ```bash
   echo "echo 'Cześć, to jest zaplanowane zadanie!'" | at 10:00 tomorrow
   ```

2. **Zaplanowanie zadania z pliku**
   Jeśli masz skrypt w pliku `backup.sh`, możesz go zaplanować na 15:00:
   ```bash
   at -f backup.sh 15:00
   ```

3. **Wyświetlenie zaplanowanych zadań**
   Aby zobaczyć wszystkie zaplanowane zadania, użyj:
   ```bash
   at -l
   ```

4. **Usunięcie zaplanowanego zadania**
   Aby usunąć zadanie o identyfikatorze 2, użyj:
   ```bash
   at -d 2
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do wykonywania zaplanowanych zadań.
- Sprawdzaj regularnie listę zaplanowanych zadań, aby uniknąć niepotrzebnych konfliktów.
- Używaj opcji `-m`, aby otrzymać powiadomienie e-mail po zakończeniu zadania, co może być przydatne w przypadku dłuższych operacji.