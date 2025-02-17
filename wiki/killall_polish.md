# [Linux] Bash killall użycie: Zakończ procesy według nazwy

## Overview
Polecenie `killall` służy do zakończenia wszystkich procesów o podanej nazwie. Jest to przydatne narzędzie do zarządzania procesami w systemie operacyjnym, umożliwiające szybkie i efektywne zamykanie aplikacji.

## Usage
Podstawowa składnia polecenia `killall` wygląda następująco:

```bash
killall [opcje] [argumenty]
```

## Common Options
- `-u, --user`: Zakończ procesy tylko dla określonego użytkownika.
- `-i, --interactive`: Potwierdź zakończenie każdego procesu.
- `-q, --quiet`: Nie wyświetlaj komunikatów o błędach.
- `-v, --verbose`: Wyświetl szczegółowe informacje o zakończonych procesach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `killall`:

1. Zakończenie wszystkich procesów o nazwie `firefox`:
   ```bash
   killall firefox
   ```

2. Zakończenie wszystkich procesów `gedit` z potwierdzeniem:
   ```bash
   killall -i gedit
   ```

3. Zakończenie procesów tylko dla użytkownika `janek`:
   ```bash
   killall -u janek
   ```

4. Zakończenie procesów `vlc` bez wyświetlania komunikatów:
   ```bash
   killall -q vlc
   ```

## Tips
- Używaj opcji `-i`, aby uniknąć przypadkowego zakończenia ważnych procesów.
- Sprawdzaj, które procesy są uruchomione przed użyciem `killall`, aby upewnić się, że zamykasz właściwe aplikacje.
- Możesz użyć `pgrep` przed `killall`, aby zobaczyć listę procesów, które zostaną zakończone:
  ```bash
  pgrep firefox
  ```