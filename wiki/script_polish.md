# [Linux] Bash script użycie: rejestracja sesji terminalowej

## Overview
Polecenie `script` służy do rejestrowania sesji terminalowej do pliku. Dzięki temu można zapisywać wszystkie polecenia oraz ich wyniki, co jest przydatne do dokumentacji lub analizy później.

## Usage
Podstawowa składnia polecenia `script` jest następująca:

```bash
script [opcje] [plik]
```

## Common Options
- `-a` – dodaje dane do istniejącego pliku zamiast go nadpisywać.
- `-f` – natychmiast zapisuje dane do pliku, co pozwala na bieżące śledzenie.
- `-q` – wycisza komunikaty o rozpoczęciu i zakończeniu rejestrowania.

## Common Examples
1. Rozpoczęcie rejestrowania sesji do pliku `output.txt`:
   ```bash
   script output.txt
   ```

2. Rozpoczęcie rejestrowania sesji i dodawanie do istniejącego pliku:
   ```bash
   script -a output.txt
   ```

3. Rejestrowanie sesji z natychmiastowym zapisywaniem:
   ```bash
   script -f output.txt
   ```

4. Użycie polecenia w trybie wyciszonym:
   ```bash
   script -q output.txt
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia do zapisu w katalogu, w którym chcesz utworzyć plik rejestru.
- Po zakończeniu sesji, aby zakończyć rejestrowanie, po prostu wpisz `exit` lub naciśnij `Ctrl+D`.
- Możesz przeglądać zapisane sesje, używając polecenia `cat` lub `less`, aby zobaczyć, co zostało zarejestrowane.