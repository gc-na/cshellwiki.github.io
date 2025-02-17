# [Linux] Bash uptime użycie: Sprawdza czas działania systemu

## Overview
Polecenie `uptime` w systemie Linux służy do wyświetlania czasu działania systemu oraz informacji o obciążeniu procesora. Dzięki temu użytkownicy mogą szybko ocenić, jak długo system działa bez przerwy oraz jakie jest aktualne obciążenie.

## Usage
Podstawowa składnia polecenia `uptime` jest następująca:

```bash
uptime [opcje]
```

## Common Options
- `-p` – wyświetla czas działania w bardziej czytelnej formie.
- `-s` – pokazuje dokładny czas, kiedy system został uruchomiony.
- `-h` – wyświetla pomoc dotycząca polecenia.

## Common Examples
1. **Podstawowe użycie:**
   ```bash
   uptime
   ```
   Wyświetla czas działania systemu oraz obciążenie procesora.

2. **Czytelna forma czasu działania:**
   ```bash
   uptime -p
   ```
   Przykład wyjścia: `System has been up for 5 hours, 23 minutes`.

3. **Czas uruchomienia systemu:**
   ```bash
   uptime -s
   ```
   Przykład wyjścia: `2023-10-01 14:30:00`.

## Tips
- Używaj opcji `-p`, aby uzyskać bardziej zrozumiałe informacje o czasie działania systemu.
- Regularne monitorowanie czasu działania może pomóc w identyfikacji problemów z wydajnością.
- Możesz zintegrować `uptime` z innymi skryptami, aby automatycznie zbierać dane o obciążeniu systemu.