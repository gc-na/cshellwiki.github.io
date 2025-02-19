# [Linux] C Shell (csh) timedatectl Użycie: zarządzanie datą i czasem systemowym

## Przegląd
Polecenie `timedatectl` jest używane do zarządzania ustawieniami daty i czasu w systemie Linux. Umożliwia użytkownikom wyświetlanie oraz modyfikowanie aktualnych ustawień czasu, strefy czasowej oraz synchronizacji czasu.

## Użycie
Podstawowa składnia polecenia `timedatectl` jest następująca:

```bash
timedatectl [opcje] [argumenty]
```

## Częste opcje
- `status` - Wyświetla aktualny stan daty, czasu i strefy czasowej.
- `set-time` - Ustawia datę i czas systemowy.
- `set-timezone` - Zmienia strefę czasową systemu.
- `set-ntp` - Włącza lub wyłącza synchronizację czasu przez NTP (Network Time Protocol).

## Częste przykłady
1. **Wyświetlenie aktualnego stanu daty i czasu:**
   ```bash
   timedatectl status
   ```

2. **Ustawienie daty i czasu na 25 grudnia 2023, godzina 15:00:**
   ```bash
   timedatectl set-time '2023-12-25 15:00:00'
   ```

3. **Zmiana strefy czasowej na Europe/Warsaw:**
   ```bash
   timedatectl set-timezone Europe/Warsaw
   ```

4. **Włączenie synchronizacji czasu przez NTP:**
   ```bash
   timedatectl set-ntp true
   ```

## Wskazówki
- Upewnij się, że masz odpowiednie uprawnienia (np. jako root), aby zmieniać ustawienia daty i czasu.
- Sprawdzaj regularnie stan synchronizacji czasu, aby uniknąć problemów z różnicą w czasie.
- Zawsze używaj pełnego formatu daty i czasu, aby uniknąć nieporozumień przy ustawianiu.