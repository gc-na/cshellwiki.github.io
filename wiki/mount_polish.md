# [Linux] C Shell (csh) mount użycie: Montowanie systemów plików

## Overview
Polecenie `mount` służy do montowania systemów plików w systemie operacyjnym. Umożliwia dostęp do danych przechowywanych na różnych nośnikach, takich jak dyski twarde, pamięci USB czy inne urządzenia.

## Usage
Podstawowa składnia polecenia `mount` jest następująca:

```
mount [opcje] [argumenty]
```

## Common Options
- `-t <typ>`: Określa typ systemu plików (np. ext4, ntfs).
- `-o <opcje>`: Umożliwia podanie dodatkowych opcji montowania (np. ro dla tylko do odczytu).
- `-a`: Montuje wszystkie systemy plików wymienione w pliku fstab.
- `-r`: Montuje system plików w trybie tylko do odczytu.

## Common Examples
1. Montowanie dysku twardego:
   ```csh
   mount /dev/sda1 /mnt
   ```

2. Montowanie pamięci USB z określeniem typu systemu plików:
   ```csh
   mount -t vfat /dev/sdb1 /media/usb
   ```

3. Montowanie systemu plików w trybie tylko do odczytu:
   ```csh
   mount -o ro /dev/sda1 /mnt
   ```

4. Montowanie wszystkich systemów plików z pliku fstab:
   ```csh
   mount -a
   ```

## Tips
- Zawsze sprawdzaj, czy urządzenie, które chcesz zamontować, jest dostępne, używając polecenia `lsblk`.
- Upewnij się, że masz odpowiednie uprawnienia do montowania urządzeń, zazwyczaj wymagane są uprawnienia administratora.
- Po zakończeniu pracy z zamontowanym systemem plików, pamiętaj o jego odmontowaniu za pomocą polecenia `umount`.