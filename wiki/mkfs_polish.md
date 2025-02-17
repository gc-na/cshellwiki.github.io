# [Linux] Bash mkfs użycie: Tworzenie systemu plików

## Overview
Polecenie `mkfs` (make filesystem) jest używane do tworzenia systemów plików na urządzeniach blokowych, takich jak dyski twarde, partycje czy pamięci USB. Dzięki `mkfs` można sformatować urządzenie, co pozwala na przechowywanie danych w zorganizowany sposób.

## Usage
Podstawowa składnia polecenia `mkfs` jest następująca:

```bash
mkfs [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `mkfs`:

- `-t <typ>`: Określa typ systemu plików do utworzenia (np. ext4, vfat).
- `-L <etykieta>`: Ustawia etykietę dla nowego systemu plików.
- `-n`: Tworzy system plików bez zapisywania na dysku (symulacja).
- `-V`: Wyświetla szczegółowe informacje o procesie tworzenia systemu plików.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `mkfs`:

1. Tworzenie systemu plików ext4 na partycji `/dev/sdb1`:

   ```bash
   mkfs -t ext4 /dev/sdb1
   ```

2. Tworzenie systemu plików FAT32 na urządzeniu USB `/dev/sdc1` z etykietą "USB_DRIVE":

   ```bash
   mkfs -t vfat -L USB_DRIVE /dev/sdc1
   ```

3. Symulacja tworzenia systemu plików bez zapisywania na dysku:

   ```bash
   mkfs -n -t ext4 /dev/sdb1
   ```

4. Wyświetlenie szczegółowych informacji podczas tworzenia systemu plików ext3:

   ```bash
   mkfs -V -t ext3 /dev/sda1
   ```

## Tips
- Zawsze upewnij się, że wybrane urządzenie jest poprawne, ponieważ `mkfs` usunie wszystkie dane na tym urządzeniu.
- Zrób kopię zapasową ważnych danych przed sformatowaniem.
- Używaj opcji `-L`, aby łatwo zidentyfikować swoje systemy plików w przyszłości.