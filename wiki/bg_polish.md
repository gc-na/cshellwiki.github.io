# [Linux] Bash bg użycie: Wznawianie zadań w tle

## Overview
Polecenie `bg` w systemie Bash służy do wznawiania zatrzymanych zadań w tle. Umożliwia to kontynuowanie pracy z procesami, które zostały wstrzymane, bez blokowania terminala.

## Usage
Podstawowa składnia polecenia `bg` jest następująca:

```bash
bg [opcje] [argumenty]
```

## Common Options
- `job_spec` - Specyfikuje zadanie, które ma być wznowione w tle. Można użyć numeru zadania lub identyfikatora procesu (PID).

## Common Examples
1. Wznowienie ostatniego zatrzymanego zadania w tle:
   ```bash
   bg
   ```

2. Wznowienie konkretnego zadania, na przykład zadania o numerze 1:
   ```bash
   bg %1
   ```

3. Wznowienie zadania z identyfikatorem procesu (PID):
   ```bash
   bg 1234
   ```

4. Wznowienie zadania w tle i kontynuowanie pracy w terminalu:
   ```bash
   sleep 100 &
   # Po zatrzymaniu zadania
   bg %1
   ```

## Tips
- Używaj polecenia `jobs`, aby sprawdzić status zatrzymanych i działających w tle zadań.
- Pamiętaj, że zadania w tle mogą generować wyjście, które może zalać terminal. Rozważ przekierowanie wyjścia do pliku.
- Aby zakończyć zadanie działające w tle, użyj polecenia `kill` z odpowiednim PID.