# [Linux] Bash tty użycie: wyświetlanie nazwy terminala

## Overview
Polecenie `tty` w systemie Linux służy do wyświetlania nazwy terminala, z którego aktualnie korzysta użytkownik. Jest to przydatne narzędzie do identyfikacji, w jakim terminalu działają skrypty lub polecenia.

## Usage
Podstawowa składnia polecenia `tty` jest następująca:

```bash
tty [opcje]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `tty`:

- `-s`: W trybie cichym, nie wyświetla żadnego wyjścia, tylko zwraca kod wyjścia.
- `--help`: Wyświetla pomoc dotyczącą polecenia `tty`.
- `--version`: Wyświetla wersję polecenia `tty`.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `tty`:

1. Wyświetlenie nazwy aktualnego terminala:
   ```bash
   tty
   ```

2. Użycie opcji cichej, aby sprawdzić, czy terminal jest interaktywny (zwraca kod wyjścia):
   ```bash
   tty -s
   echo $?
   ```

3. Wyświetlenie pomocy dotyczącej polecenia `tty`:
   ```bash
   tty --help
   ```

4. Sprawdzenie wersji polecenia `tty`:
   ```bash
   tty --version
   ```

## Tips
- Używaj `tty` w skryptach, aby upewnić się, że skrypt działa w odpowiednim terminalu.
- Opcja `-s` jest przydatna w skryptach do sprawdzania, czy skrypt jest uruchamiany w interaktywnym terminalu.
- Pamiętaj, że `tty` zwraca różne wyniki w zależności od tego, jak uruchamiasz terminal (np. wirtualny terminal vs. terminal graficzny).