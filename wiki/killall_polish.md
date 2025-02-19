# [Linux] C Shell (csh) killall użycie: Zakończ procesy według nazwy

## Overview
Polecenie `killall` w C Shell (csh) służy do zakończenia wszystkich procesów o określonej nazwie. Jest to przydatne narzędzie, gdy chcesz szybko zamknąć wiele instancji programu bez konieczności identyfikowania ich identyfikatorów procesów (PID).

## Usage
Podstawowa składnia polecenia `killall` jest następująca:

```
killall [opcje] [argumenty]
```

## Common Options
- `-u <użytkownik>`: Zakończ procesy tylko dla określonego użytkownika.
- `-s <sygnał>`: Wyślij określony sygnał do procesów (domyślnie jest to SIGTERM).
- `-q`: Nie wyświetlaj komunikatów o błędach, jeśli nie ma procesów do zakończenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `killall`:

1. Zakończenie wszystkich procesów o nazwie `firefox`:
   ```csh
   killall firefox
   ```

2. Zakończenie wszystkich procesów `gedit` z wysłaniem sygnału SIGKILL:
   ```csh
   killall -s SIGKILL gedit
   ```

3. Zakończenie procesów `python` tylko dla użytkownika `janek`:
   ```csh
   killall -u janek python
   ```

4. Zakończenie procesów `myapp`, nie wyświetlając komunikatów o błędach:
   ```csh
   killall -q myapp
   ```

## Tips
- Używaj `killall` ostrożnie, aby nie zakończyć procesów, które mogą być potrzebne do działania systemu.
- Zawsze sprawdzaj, które procesy są uruchomione, używając polecenia `ps`, zanim użyjesz `killall`.
- Możesz użyć opcji `-s` z różnymi sygnałami, aby dostosować sposób zakończenia procesów, na przykład `SIGTERM` lub `SIGKILL`.