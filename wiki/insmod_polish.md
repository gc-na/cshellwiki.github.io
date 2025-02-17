# [Linux] Bash insmod użycie: Wczytywanie modułów jądra

## Overview
Polecenie `insmod` służy do wczytywania modułów jądra w systemie Linux. Umożliwia dodawanie nowych funkcji do jądra bez potrzeby restartowania systemu. Jest to przydatne, gdy chcemy rozszerzyć możliwości systemu o dodatkowe sterowniki lub funkcje.

## Usage
Podstawowa składnia polecenia `insmod` jest następująca:

```bash
insmod [opcje] [argumenty]
```

## Common Options
- `-f`: Wymusza wczytanie modułu, nawet jeśli nie jest on zgodny z bieżącą wersją jądra.
- `-n`: Umożliwia podanie alternatywnej nazwy dla modułu.
- `--dry-run`: Symuluje wczytanie modułu, nie dokonując rzeczywistych zmian.

## Common Examples
1. Wczytanie modułu o nazwie `mymodule.ko`:
   ```bash
   insmod mymodule.ko
   ```

2. Wczytanie modułu z wymuszeniem:
   ```bash
   insmod -f mymodule.ko
   ```

3. Wczytanie modułu z alternatywną nazwą:
   ```bash
   insmod -n mymodule_alias mymodule.ko
   ```

4. Symulacja wczytania modułu:
   ```bash
   insmod --dry-run mymodule.ko
   ```

## Tips
- Zawsze sprawdzaj, czy moduł, który chcesz wczytać, jest zgodny z wersją jądra, aby uniknąć problemów z systemem.
- Używaj `lsmod`, aby zobaczyć listę aktualnie wczytanych modułów.
- Po wczytaniu modułu, możesz użyć `dmesg`, aby sprawdzić logi systemowe i upewnić się, że moduł został poprawnie załadowany.