# [Linux] Bash ps użycie: wyświetlanie informacji o procesach

## Overview
Polecenie `ps` (process status) służy do wyświetlania informacji o bieżących procesach działających w systemie. Umożliwia monitorowanie aktywności systemu oraz zarządzanie procesami.

## Usage
Podstawowa składnia polecenia `ps` jest następująca:

```bash
ps [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `ps`:

- `-e` lub `-A`: Wyświetla wszystkie procesy w systemie.
- `-f`: Wyświetla pełny format informacji o procesach, w tym identyfikatory rodziców.
- `-u [użytkownik]`: Wyświetla procesy dla określonego użytkownika.
- `-aux`: Wyświetla szczegółowe informacje o wszystkich procesach, w tym te, które nie mają terminala.
- `--sort`: Sortuje wyniki według określonego kryterium, np. `--sort=-%mem` sortuje według użycia pamięci.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ps`:

1. Wyświetlenie wszystkich procesów działających w systemie:
   ```bash
   ps -e
   ```

2. Wyświetlenie procesów w formacie pełnym:
   ```bash
   ps -f
   ```

3. Wyświetlenie procesów dla konkretnego użytkownika:
   ```bash
   ps -u username
   ```

4. Wyświetlenie wszystkich procesów z detalami:
   ```bash
   ps aux
   ```

5. Sortowanie procesów według użycia pamięci:
   ```bash
   ps aux --sort=-%mem
   ```

## Tips
- Używaj opcji `-f` w połączeniu z `-e`, aby uzyskać bardziej szczegółowe informacje o procesach.
- Możesz użyć `grep`, aby filtrować wyniki, na przykład:
  ```bash
  ps aux | grep firefox
  ```
- Regularne monitorowanie procesów może pomóc w identyfikacji problemów z wydajnością systemu.