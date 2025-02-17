# [Linux] Bash jobs użycie: zarządzanie procesami w tle

## Overview
Polecenie `jobs` w Bash służy do wyświetlania listy zadań uruchomionych w bieżącej powłoce, które są w tle lub wstrzymane. Umożliwia użytkownikowi monitorowanie i zarządzanie procesami, które nie są aktualnie aktywne w terminalu.

## Usage
Podstawowa składnia polecenia `jobs` jest następująca:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Wyświetla identyfikatory procesów (PID) dla zadań.
- `-n`: Wyświetla tylko te zadania, które zmieniły swój stan od ostatniego wywołania `jobs`.
- `-p`: Wyświetla tylko identyfikatory procesów (PID) zadań.

## Common Examples
1. **Wyświetlenie wszystkich zadań**:
   ```bash
   jobs
   ```

2. **Wyświetlenie zadań z identyfikatorami procesów**:
   ```bash
   jobs -l
   ```

3. **Wyświetlenie tylko zadań, które zmieniły stan**:
   ```bash
   jobs -n
   ```

4. **Wyświetlenie identyfikatorów procesów zadań**:
   ```bash
   jobs -p
   ```

## Tips
- Użyj `bg` i `fg` w połączeniu z `jobs`, aby wznowić wstrzymane zadania w tle lub na pierwszym planie.
- Regularnie sprawdzaj status zadań, aby upewnić się, że nie są one w stanie wstrzymania przez dłuższy czas.
- Pamiętaj, że `jobs` działa tylko w kontekście bieżącej powłoki, więc nie zobaczysz zadań uruchomionych w innych terminalach.