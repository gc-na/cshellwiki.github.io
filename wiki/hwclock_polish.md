# [Linux] Bash hwclock użycie: synchronizacja czasu systemowego z zegarem sprzętowym

## Przegląd
Polecenie `hwclock` służy do odczytu i ustawiania czasu zegara sprzętowego (RTC - Real Time Clock) w systemie operacyjnym. Umożliwia synchronizację czasu systemowego z zegarem sprzętowym oraz odwrotnie, co jest istotne dla prawidłowego funkcjonowania systemu.

## Użycie
Podstawowa składnia polecenia `hwclock` jest następująca:

```bash
hwclock [opcje] [argumenty]
```

## Często używane opcje
- `--show` - wyświetla aktualny czas zegara sprzętowego.
- `--set` - ustawia czas zegara sprzętowego na podstawie podanych wartości.
- `--hctosys` - synchronizuje czas systemowy z zegarem sprzętowym.
- `--systohc` - ustawia zegar sprzętowy na czas systemowy.
- `--utc` - traktuje czas jako czas uniwersalny (UTC).

## Przykłady
1. **Wyświetlenie aktualnego czasu zegara sprzętowego:**
   ```bash
   hwclock --show
   ```

2. **Ustawienie zegara sprzętowego na określoną datę i czas:**
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. **Synchronizacja czasu systemowego z zegarem sprzętowym:**
   ```bash
   hwclock --hctosys
   ```

4. **Ustawienie zegara sprzętowego na czas systemowy:**
   ```bash
   hwclock --systohc
   ```

5. **Wyświetlenie czasu w formacie UTC:**
   ```bash
   hwclock --show --utc
   ```

## Wskazówki
- Upewnij się, że masz odpowiednie uprawnienia (zazwyczaj wymagane są uprawnienia administratora) do wykonywania operacji na zegarze sprzętowym.
- Regularnie synchronizuj czas systemowy z zegarem sprzętowym, aby uniknąć problemów z czasem w systemie.
- Sprawdź, czy twój system jest skonfigurowany do używania czasu lokalnego lub UTC, aby uniknąć nieporozumień przy ustawianiu czasu.