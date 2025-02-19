# [Linux] C Shell (csh) journalctl użycie: przeglądanie logów systemowych

## Overview
`journalctl` to polecenie używane do przeglądania logów systemowych w systemach Linux, które korzystają z systemd. Umożliwia dostęp do informacji o zdarzeniach systemowych, co jest przydatne do diagnostyki i monitorowania.

## Usage
Podstawowa składnia polecenia `journalctl` jest następująca:

```csh
journalctl [options] [arguments]
```

## Common Options
- `-b` – wyświetla logi od ostatniego uruchomienia systemu.
- `-f` – śledzi na żywo nowe wpisy w logach.
- `--since` – pozwala na określenie daty początkowej do przeszukiwania logów.
- `--until` – pozwala na określenie daty końcowej do przeszukiwania logów.
- `-u <nazwa_usługi>` – filtruje logi dla określonej usługi systemd.

## Common Examples
Oto kilka praktycznych przykładów użycia `journalctl`:

1. Wyświetlenie wszystkich logów:
   ```csh
   journalctl
   ```

2. Wyświetlenie logów od ostatniego uruchomienia systemu:
   ```csh
   journalctl -b
   ```

3. Śledzenie nowych wpisów w logach na żywo:
   ```csh
   journalctl -f
   ```

4. Wyświetlenie logów dla konkretnej usługi, np. `nginx`:
   ```csh
   journalctl -u nginx
   ```

5. Wyświetlenie logów w określonym przedziale czasowym:
   ```csh
   journalctl --since "2023-10-01" --until "2023-10-10"
   ```

## Tips
- Używaj opcji `-f`, aby na bieżąco monitorować logi, co jest szczególnie przydatne podczas rozwiązywania problemów.
- Filtruj logi według usług, aby skupić się na interesujących cię komponentach systemu.
- Regularnie przeglądaj logi, aby wykrywać potencjalne problemy zanim staną się poważne.