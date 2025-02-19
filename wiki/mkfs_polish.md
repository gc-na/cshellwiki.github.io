# [Linux] C Shell (csh) mkfs użycie: Tworzenie systemu plików

## Overview
Polecenie `mkfs` (make filesystem) służy do tworzenia systemu plików na partycji lub urządzeniu blokowym. Umożliwia formatowanie nośników danych, takich jak dyski twarde, pamięci USB czy inne urządzenia magazynujące.

## Usage
Podstawowa składnia polecenia `mkfs` jest następująca:

```csh
mkfs [opcje] [argumenty]
```

## Common Options
- `-t <typ>`: Określa typ systemu plików do utworzenia (np. ext4, vfat).
- `-L <etykieta>`: Ustala etykietę dla nowego systemu plików.
- `-n`: Tworzy system plików bez formatowania (przydatne do testów).
- `-V`: Wyświetla szczegółowe informacje o procesie tworzenia systemu plików.

## Common Examples
1. Tworzenie systemu plików ext4 na urządzeniu `/dev/sdb1`:
   ```csh
   mkfs -t ext4 /dev/sdb1
   ```

2. Tworzenie systemu plików vfat z etykietą "USB_DRIVE":
   ```csh
   mkfs -t vfat -L USB_DRIVE /dev/sdc1
   ```

3. Tworzenie systemu plików bez formatowania (test):
   ```csh
   mkfs -n /dev/sda1
   ```

4. Wyświetlanie szczegółowych informacji podczas tworzenia systemu plików:
   ```csh
   mkfs -V -t ext3 /dev/sdd1
   ```

## Tips
- Zawsze upewnij się, że wybrane urządzenie jest poprawne, aby uniknąć przypadkowego usunięcia danych.
- Przed użyciem `mkfs`, warto wykonać kopię zapasową ważnych danych.
- Sprawdź, czy masz odpowiednie uprawnienia do formatowania urządzenia (może być wymagane użycie `sudo`).
- Używaj opcji `-n` do testowania, zanim zdecydujesz się na faktyczne formatowanie.