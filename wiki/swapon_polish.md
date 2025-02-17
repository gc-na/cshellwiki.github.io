# [Linux] Bash swapon użycie: Włączanie przestrzeni wymiany

## Overview
Polecenie `swapon` służy do aktywacji przestrzeni wymiany (swap) w systemie Linux. Przestrzeń wymiany jest używana przez system operacyjny do przechowywania danych, które nie mieszczą się w pamięci RAM, co pozwala na efektywniejsze zarządzanie pamięcią.

## Usage
Podstawowa składnia polecenia `swapon` jest następująca:

```bash
swapon [opcje] [argumenty]
```

## Common Options
- `-a` – Aktywuje wszystkie urządzenia wymiany wymienione w pliku `/etc/fstab`.
- `-e` – Sprawdza, czy przestrzeń wymiany jest poprawna przed jej aktywacją.
- `-s` – Wyświetla informacje o aktywnych przestrzeniach wymiany.

## Common Examples
1. Aktywacja przestrzeni wymiany zdefiniowanej w pliku `/etc/fstab`:
   ```bash
   swapon -a
   ```

2. Aktywacja konkretnego pliku wymiany:
   ```bash
   swapon /path/to/swapfile
   ```

3. Sprawdzenie aktywnych przestrzeni wymiany:
   ```bash
   swapon -s
   ```

4. Aktywacja przestrzeni wymiany z weryfikacją:
   ```bash
   swapon -e /path/to/swapfile
   ```

## Tips
- Upewnij się, że przestrzeń wymiany została poprawnie utworzona przed jej aktywacją.
- Regularnie sprawdzaj status przestrzeni wymiany, aby upewnić się, że system działa optymalnie.
- Rozważ użycie `swapon -a` po każdorazowym uruchomieniu systemu, aby automatycznie aktywować przestrzenie wymiany.