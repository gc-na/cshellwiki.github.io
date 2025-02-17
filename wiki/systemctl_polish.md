# [Linux] Bash systemctl użycie: Zarządzanie usługami systemowymi

## Overview
Polecenie `systemctl` jest narzędziem do zarządzania systemem i usługami w systemach opartych na systemd. Umożliwia uruchamianie, zatrzymywanie, restartowanie oraz sprawdzanie statusu usług systemowych.

## Usage
Podstawowa składnia polecenia `systemctl` jest następująca:

```
systemctl [opcje] [argumenty]
```

## Common Options
- `start`: Uruchamia określoną usługę.
- `stop`: Zatrzymuje określoną usługę.
- `restart`: Restartuje określoną usługę.
- `status`: Wyświetla status określonej usługi.
- `enable`: Włącza usługę, aby uruchamiała się automatycznie przy starcie systemu.
- `disable`: Wyłącza automatyczne uruchamianie usługi przy starcie systemu.
- `list-units`: Wyświetla listę wszystkich jednostek (usług) w systemie.

## Common Examples
1. **Uruchamianie usługi**
   ```bash
   systemctl start nazwa_usługi
   ```

2. **Zatrzymywanie usługi**
   ```bash
   systemctl stop nazwa_usługi
   ```

3. **Restartowanie usługi**
   ```bash
   systemctl restart nazwa_usługi
   ```

4. **Sprawdzanie statusu usługi**
   ```bash
   systemctl status nazwa_usługi
   ```

5. **Włączanie usługi przy starcie systemu**
   ```bash
   systemctl enable nazwa_usługi
   ```

6. **Wyłączanie usługi przy starcie systemu**
   ```bash
   systemctl disable nazwa_usługi
   ```

7. **Wyświetlanie listy wszystkich usług**
   ```bash
   systemctl list-units --type=service
   ```

## Tips
- Używaj `sudo` przed poleceniem `systemctl`, aby uzyskać uprawnienia administratora, jeśli operujesz na usługach systemowych.
- Regularnie sprawdzaj status usług, aby upewnić się, że działają poprawnie.
- Zapisuj logi systemowe, aby móc analizować problemy z usługami w przyszłości.