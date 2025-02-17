# [Linux] Bash watch użycie: Monitorowanie poleceń w czasie rzeczywistym

## Overview
Polecenie `watch` w systemie Linux służy do wykonywania innego polecenia w regularnych odstępach czasu, co pozwala na monitorowanie jego wyników w czasie rzeczywistym. Jest to przydatne narzędzie do obserwacji zmian w danych lub statusie systemu.

## Usage
Podstawowa składnia polecenia `watch` jest następująca:

```
watch [opcje] [argumenty]
```

## Common Options
- `-n, --interval`: Ustala interwał czasowy w sekundach, co ile polecenie ma być wykonywane (domyślnie co 2 sekundy).
- `-d, --differences`: Podświetla różnice między kolejnymi wynikami.
- `-t, --no-title`: Ukrywa nagłówek wyświetlany na górze okna.
- `-x, --exec`: Wykonuje polecenie z podanymi argumentami.

## Common Examples
1. Monitorowanie użycia pamięci:
   ```bash
   watch -n 5 free -h
   ```

2. Obserwacja katalogu w poszukiwaniu nowych plików:
   ```bash
   watch -n 10 ls -l /path/to/directory
   ```

3. Sprawdzanie statusu procesów:
   ```bash
   watch -d ps aux | grep my_process
   ```

4. Monitorowanie logów systemowych:
   ```bash
   watch -n 1 tail -n 20 /var/log/syslog
   ```

## Tips
- Używaj opcji `-d`, aby szybko zauważyć zmiany w wynikach.
- Dostosuj interwał czasowy do swoich potrzeb, aby uniknąć nadmiernego obciążenia systemu.
- Możesz łączyć `watch` z innymi poleceniami, aby uzyskać bardziej złożone wyniki.