# [Linux] Bash fsck użycie: Sprawdzanie i naprawa systemu plików

## Przegląd
Polecenie `fsck` (file system check) służy do sprawdzania integralności systemu plików w systemie Linux. Umożliwia wykrywanie i naprawę błędów, które mogą wystąpić w systemach plików, co jest istotne dla zapewnienia ich prawidłowego działania.

## Użycie
Podstawowa składnia polecenia `fsck` wygląda następująco:

```bash
fsck [opcje] [argumenty]
```

## Częste opcje
- `-a` – automatycznie naprawia błędy bez interakcji z użytkownikiem.
- `-n` – wykonuje sprawdzenie, ale nie dokonuje żadnych zmian (tryb tylko do odczytu).
- `-y` – automatycznie odpowiada "tak" na wszystkie pytania o naprawę.
- `-t` – wyświetla szczegółowe informacje o czasie wykonania sprawdzenia.

## Częste przykłady
1. Sprawdzenie systemu plików na urządzeniu `/dev/sda1`:
   ```bash
   fsck /dev/sda1
   ```

2. Automatyczna naprawa błędów na systemie plików:
   ```bash
   fsck -a /dev/sda1
   ```

3. Sprawdzenie systemu plików bez wprowadzania zmian:
   ```bash
   fsck -n /dev/sda1
   ```

4. Automatyczne potwierdzanie naprawy błędów:
   ```bash
   fsck -y /dev/sda1
   ```

## Wskazówki
- Zawsze wykonuj `fsck` na odmontowanym systemie plików, aby uniknąć uszkodzenia danych.
- Regularnie sprawdzaj system plików, aby zapobiec poważnym problemom.
- Używaj opcji `-n` w celu przeprowadzenia testów przed wprowadzeniem jakichkolwiek zmian, zwłaszcza na ważnych systemach produkcyjnych.