# [Linux] C Shell (csh) parted użycie: Zarządzanie partycjami dyskowymi

## Overview
Polecenie `parted` służy do zarządzania partycjami dyskowymi. Umożliwia użytkownikom tworzenie, usuwanie, zmienianie rozmiaru i modyfikowanie partycji na dyskach twardych oraz innych nośnikach danych.

## Usage
Podstawowa składnia polecenia `parted` wygląda następująco:

```bash
parted [opcje] [argumenty]
```

## Common Options
- `-l` : Wyświetla listę wszystkich dostępnych dysków i ich partycji.
- `mkpart` : Tworzy nową partycję.
- `rm` : Usuwa istniejącą partycję.
- `resizepart` : Zmienia rozmiar istniejącej partycji.
- `print` : Wyświetla szczegóły dotyczące partycji na wybranym dysku.

## Common Examples
1. **Wyświetlenie listy dysków i partycji:**
   ```bash
   parted -l
   ```

2. **Tworzenie nowej partycji:**
   ```bash
   parted /dev/sda mkpart primary ext4 1MiB 100MiB
   ```

3. **Usuwanie partycji:**
   ```bash
   parted /dev/sda rm 1
   ```

4. **Zmiana rozmiaru partycji:**
   ```bash
   parted /dev/sda resizepart 1 200MiB
   ```

5. **Wyświetlenie szczegółów partycji:**
   ```bash
   parted /dev/sda print
   ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed modyfikacją partycji, aby uniknąć utraty danych.
- Używaj polecenia `print` przed i po zmianach, aby upewnić się, że operacje zostały wykonane poprawnie.
- Upewnij się, że nie masz otwartych plików lub systemów plików na partycjach, które chcesz modyfikować.