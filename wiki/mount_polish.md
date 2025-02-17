# [Linux] Bash mount użycie: Montowanie systemów plików

## Overview
Polecenie `mount` w systemach Unix i Linux służy do montowania systemów plików. Umożliwia dostęp do danych przechowywanych na różnych urządzeniach, takich jak dyski twarde, pamięci USB czy sieciowe systemy plików.

## Usage
Podstawowa składnia polecenia `mount` jest następująca:

```bash
mount [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `mount`:

- `-t` : Określa typ systemu plików (np. ext4, ntfs).
- `-o` : Umożliwia podanie dodatkowych opcji montowania, takich jak `ro` (tylko do odczytu) lub `rw` (do odczytu i zapisu).
- `-a` : Montuje wszystkie systemy plików wymienione w pliku `/etc/fstab`.
- `-r` : Montuje system plików w trybie tylko do odczytu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `mount`:

1. Montowanie dysku USB:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```

2. Montowanie systemu plików NTFS w trybie tylko do odczytu:
   ```bash
   mount -t ntfs -o ro /dev/sdc1 /mnt/ntfs
   ```

3. Montowanie wszystkich systemów plików z pliku fstab:
   ```bash
   mount -a
   ```

4. Montowanie systemu plików ext4 z dodatkowymi opcjami:
   ```bash
   mount -t ext4 -o rw,noatime /dev/sda1 /mnt/data
   ```

## Tips
- Zawsze upewnij się, że punkt montowania (np. `/mnt/usb`) istnieje przed próbą montowania.
- Używaj opcji `-o ro`, jeśli chcesz zabezpieczyć dane przed przypadkowym zapisem.
- Sprawdź, czy system plików jest poprawnie odmontowany przed odłączeniem urządzenia, używając polecenia `umount`.