# [Linux] Bash fg użycie: Przywraca zadanie do pierwszego planu

## Overview
Polecenie `fg` w Bashu służy do przywracania zadań, które zostały uruchomione w tle, do pierwszego planu. Dzięki temu użytkownik może kontynuować interakcję z danym procesem, który wcześniej został zminimalizowany lub uruchomiony w tle.

## Usage
Podstawowa składnia polecenia `fg` jest następująca:

```bash
fg [numer_zadania]
```

## Common Options
- `numer_zadania`: Opcjonalny argument, który wskazuje, które zadanie ma być przywrócone do pierwszego planu. Można użyć numeru zadania lub prefiksu `%`, np. `%1` dla pierwszego zadania.

## Common Examples
1. Przywrócenie pierwszego zadania do pierwszego planu:
   ```bash
   fg %1
   ```

2. Przywrócenie drugiego zadania do pierwszego planu:
   ```bash
   fg %2
   ```

3. Przywrócenie ostatniego zatrzymanego zadania:
   ```bash
   fg
   ```

## Tips
- Użyj polecenia `jobs`, aby zobaczyć listę wszystkich zadań i ich numery przed przywróceniem ich do pierwszego planu.
- Możesz używać `Ctrl + Z`, aby zatrzymać bieżące zadanie i przenieść je do tła, a następnie użyć `fg`, aby je przywrócić.
- Pamiętaj, że przywrócone zadanie będzie miało dostęp do terminala, co oznacza, że możesz z nim wchodzić w interakcje tak, jakby było uruchomione w pierwszym planie od początku.