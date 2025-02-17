# [Linux] Użytkownicy Bash: Zarządzanie użytkownikami systemu

## Overview
Polecenie `users` w systemie Linux służy do wyświetlania nazw użytkowników, którzy są aktualnie zalogowani na systemie. Jest to przydatne narzędzie do szybkiego sprawdzenia, którzy użytkownicy są aktywni w danym momencie.

## Usage
Podstawowa składnia polecenia `users` jest następująca:

```bash
users [opcje]
```

## Common Options
- `-H`, `--help`: Wyświetla pomoc dotyczącą polecenia.
- `-V`, `--version`: Wyświetla wersję polecenia.

## Common Examples
1. **Wyświetlenie zalogowanych użytkowników:**
   ```bash
   users
   ```

2. **Wyświetlenie pomocy:**
   ```bash
   users --help
   ```

3. **Wyświetlenie wersji:**
   ```bash
   users --version
   ```

## Tips
- Użyj polecenia `who` lub `w`, aby uzyskać bardziej szczegółowe informacje o zalogowanych użytkownikach, takie jak czas logowania i aktywność.
- Polecenie `users` jest szczególnie przydatne w skryptach, gdzie potrzebujesz szybko sprawdzić, którzy użytkownicy są aktualnie zalogowani.