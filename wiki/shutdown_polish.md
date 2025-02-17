# [Linux] Bash shutdown użycie: Zamykanie systemu

## Overview
Polecenie `shutdown` służy do bezpiecznego zamykania systemu operacyjnego. Umożliwia administratorom planowanie zamknięcia systemu w określonym czasie lub natychmiastowe wyłączenie komputera.

## Usage
Podstawowa składnia polecenia `shutdown` jest następująca:

```
shutdown [opcje] [argumenty]
```

## Common Options
- `-h` lub `--halt`: Zatrzymuje system po zamknięciu.
- `-r` lub `--reboot`: Uruchamia system ponownie po zamknięciu.
- `-P` lub `--poweroff`: Wyłącza system po zamknięciu.
- `now`: Natychmiastowe zamknięcie systemu.
- `+m`: Zamknięcie systemu po upływie m minut (np. `+5` zamknie system za 5 minut).

## Common Examples
- Aby natychmiast zamknąć system:
  ```bash
  shutdown now
  ```

- Aby zaplanować zamknięcie systemu za 10 minut:
  ```bash
  shutdown +10
  ```

- Aby zrestartować system:
  ```bash
  shutdown -r now
  ```

- Aby wyłączyć system:
  ```bash
  shutdown -h now
  ```

- Aby zamknąć system o określonej godzinie (np. 22:00):
  ```bash
  shutdown 22:00
  ```

## Tips
- Zawsze upewnij się, że wszyscy użytkownicy są poinformowani o planowanym zamknięciu systemu, aby uniknąć utraty danych.
- Możesz użyć opcji `-c`, aby anulować zaplanowane zamknięcie, jeśli zajdzie taka potrzeba.
- Rozważ użycie `shutdown` w skryptach automatyzujących, aby zarządzać zamykaniem systemu w regularnych odstępach czasu.