# [Linux] Bash rmmod: Usuwanie modułów jądra

## Overview
Polecenie `rmmod` służy do usuwania modułów jądra w systemie Linux. Moduły te są dynamicznie ładowanymi komponentami, które rozszerzają funkcjonalność jądra, umożliwiając dodawanie nowych sterowników lub funkcji bez konieczności ponownego uruchamiania systemu.

## Usage
Podstawowa składnia polecenia `rmmod` jest następująca:

```
rmmod [opcje] [argumenty]
```

## Common Options
- `-f` – wymusza usunięcie modułu, nawet jeśli jest on aktualnie używany.
- `-n` – nie wyświetla komunikatów o błędach.
- `--help` – wyświetla pomoc dotyczącą użycia polecenia.
- `--version` – wyświetla wersję polecenia.

## Common Examples
1. Usunięcie modułu o nazwie `mymodule`:
    ```bash
    rmmod mymodule
    ```

2. Wymuszenie usunięcia modułu, nawet jeśli jest używany:
    ```bash
    rmmod -f mymodule
    ```

3. Wyświetlenie pomocy dotyczącej polecenia:
    ```bash
    rmmod --help
    ```

4. Sprawdzenie wersji polecenia:
    ```bash
    rmmod --version
    ```

## Tips
- Zawsze sprawdzaj, czy moduł nie jest aktualnie używany przed jego usunięciem, aby uniknąć problemów z systemem.
- Używaj opcji `-f` ostrożnie, ponieważ może to prowadzić do niestabilności systemu.
- Regularnie monitoruj załadowane moduły za pomocą polecenia `lsmod`, aby zrozumieć, które moduły są aktywne w Twoim systemie.