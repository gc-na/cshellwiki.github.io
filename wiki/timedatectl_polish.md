# [Linux] Bash timedatectl użycie: Zarządzanie datą i czasem systemu

## Overview
Polecenie `timedatectl` jest używane do zarządzania ustawieniami daty i czasu w systemach Linux. Umożliwia użytkownikom wyświetlanie i modyfikowanie informacji o czasie, strefach czasowych oraz synchronizacji czasu.

## Usage
Podstawowa składnia polecenia `timedatectl` wygląda następująco:

```bash
timedatectl [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `timedatectl`:

- `status` - Wyświetla aktualny stan daty i czasu oraz strefy czasowej.
- `set-time` - Ustawia datę i czas systemowy.
- `set-timezone` - Ustawia strefę czasową systemu.
- `set-ntp` - Włącza lub wyłącza synchronizację czasu przez NTP (Network Time Protocol).
- `list-timezones` - Wyświetla listę dostępnych stref czasowych.

## Common Examples
Oto kilka praktycznych przykładów użycia `timedatectl`:

1. **Wyświetlenie aktualnego stanu daty i czasu:**
   ```bash
   timedatectl status
   ```

2. **Ustawienie daty i czasu na 1 stycznia 2023 roku, 12:00:00:**
   ```bash
   timedatectl set-time '2023-01-01 12:00:00'
   ```

3. **Ustawienie strefy czasowej na Warszawę:**
   ```bash
   timedatectl set-timezone Europe/Warsaw
   ```

4. **Włączenie synchronizacji czasu przez NTP:**
   ```bash
   timedatectl set-ntp true
   ```

5. **Wyświetlenie dostępnych stref czasowych:**
   ```bash
   timedatectl list-timezones
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia, aby zmieniać ustawienia daty i czasu (może być wymagane użycie `sudo`).
- Regularnie sprawdzaj status synchronizacji NTP, aby upewnić się, że czas systemowy jest zawsze dokładny.
- Zawsze używaj pełnych dat i godzin w formacie `YYYY-MM-DD HH:MM:SS`, aby uniknąć nieporozumień.