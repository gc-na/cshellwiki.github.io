# [Linux] Bash journalctl użycie: Przeglądanie dzienników systemowych

## Overview
Polecenie `journalctl` jest używane do przeglądania dzienników systemowych w systemach opartych na systemd. Umożliwia dostęp do logów, które są zbierane przez systemd-journald, co pozwala na monitorowanie i diagnozowanie problemów w systemie.

## Usage
Podstawowa składnia polecenia `journalctl` wygląda następująco:

```bash
journalctl [opcje] [argumenty]
```

## Common Options
- `-b` – Wyświetla logi od ostatniego uruchomienia systemu.
- `-f` – Śledzi na żywo nowe wpisy w dzienniku.
- `--since` – Filtruje logi od określonego czasu (np. `--since "2023-10-01"`).
- `--until` – Filtruje logi do określonego czasu (np. `--until "2023-10-02"`).
- `-u` – Wyświetla logi dla konkretnej jednostki systemd (np. `-u nginx.service`).

## Common Examples
1. **Wyświetlenie wszystkich logów:**
   ```bash
   journalctl
   ```

2. **Wyświetlenie logów od ostatniego uruchomienia systemu:**
   ```bash
   journalctl -b
   ```

3. **Śledzenie nowych wpisów w dzienniku:**
   ```bash
   journalctl -f
   ```

4. **Filtracja logów od konkretnej daty:**
   ```bash
   journalctl --since "2023-10-01"
   ```

5. **Wyświetlenie logów dla konkretnej usługi:**
   ```bash
   journalctl -u ssh.service
   ```

## Tips
- Używaj opcji `-f`, aby na bieżąco monitorować logi, co jest przydatne podczas rozwiązywania problemów.
- Kombinuj opcje `--since` i `--until`, aby precyzyjnie określić zakres czasowy logów, które chcesz przeglądać.
- Pamiętaj, że logi mogą być bardzo obszerne, więc warto używać filtrów, aby skupić się na interesujących cię informacjach.