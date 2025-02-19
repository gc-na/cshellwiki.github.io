# [Linux] C Shell (csh) fsck: Sprawdzanie systemu plików

## Overview
Polecenie `fsck` (file system check) jest używane do sprawdzania i naprawiania systemów plików w systemach Unix i Linux. Pomaga w identyfikacji i naprawie błędów w strukturze systemu plików, co jest szczególnie przydatne po nieprawidłowym zamknięciu systemu lub awarii.

## Usage
Podstawowa składnia polecenia `fsck` jest następująca:

```
fsck [opcje] [argumenty]
```

## Common Options
- `-a`: Automatycznie naprawia błędy bez interakcji z użytkownikiem.
- `-n`: Sprawdza system plików, ale nie wprowadza żadnych zmian.
- `-y`: Odpowiada "tak" na wszystkie pytania, co oznacza automatyczne naprawianie błędów.
- `-t`: Wyświetla czas wykonania polecenia.

## Common Examples
Przykłady użycia polecenia `fsck`:

1. Sprawdzenie systemu plików na urządzeniu `/dev/sda1`:
   ```bash
   fsck /dev/sda1
   ```

2. Automatyczna naprawa błędów w systemie plików:
   ```bash
   fsck -a /dev/sda1
   ```

3. Sprawdzenie systemu plików bez wprowadzania zmian:
   ```bash
   fsck -n /dev/sda1
   ```

4. Automatyczne naprawianie błędów z potwierdzeniem:
   ```bash
   fsck -y /dev/sda1
   ```

## Tips
- Zawsze wykonuj kopię zapasową ważnych danych przed użyciem `fsck`, aby uniknąć utraty danych w przypadku poważnych błędów.
- Używaj `fsck` w trybie jednego użytkownika lub z systemem uruchomionym z nośnika ratunkowego, aby uniknąć problemów z otwartymi plikami.
- Regularnie sprawdzaj system plików, aby zapobiec poważnym problemom w przyszłości.