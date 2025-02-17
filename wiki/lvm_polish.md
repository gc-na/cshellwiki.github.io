# [Linux] Bash lvm użycie: Zarządzanie woluminami logicznymi

## Overview
Polecenie `lvm` (Logical Volume Manager) jest używane do zarządzania woluminami logicznymi w systemach Linux. Umożliwia tworzenie, usuwanie i modyfikowanie woluminów logicznych oraz grup woluminów, co pozwala na elastyczne zarządzanie przestrzenią dyskową.

## Usage
Podstawowa składnia polecenia `lvm` jest następująca:

```bash
lvm [opcje] [argumenty]
```

## Common Options
- `vgcreate`: Tworzy nową grupę woluminów.
- `lvcreate`: Tworzy nowy wolumin logiczny.
- `lvremove`: Usuwa wolumin logiczny.
- `lvextend`: Zwiększa rozmiar woluminu logicznego.
- `lvreduce`: Zmniejsza rozmiar woluminu logicznego.
- `vgextend`: Dodaje fizyczne wolumeny do grupy woluminów.

## Common Examples
1. **Tworzenie grupy woluminów**:
   ```bash
   vgcreate my_volume_group /dev/sdb1 /dev/sdc1
   ```

2. **Tworzenie woluminu logicznego**:
   ```bash
   lvcreate -n my_logical_volume -L 10G my_volume_group
   ```

3. **Usuwanie woluminu logicznego**:
   ```bash
   lvremove /dev/my_volume_group/my_logical_volume
   ```

4. **Zwiększanie rozmiaru woluminu logicznego**:
   ```bash
   lvextend -L +5G /dev/my_volume_group/my_logical_volume
   ```

5. **Zmniejszanie rozmiaru woluminu logicznego**:
   ```bash
   lvreduce -L -5G /dev/my_volume_group/my_logical_volume
   ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed modyfikacją woluminów logicznych.
- Używaj opcji `-n` przy tworzeniu woluminów logicznych, aby nadać im czytelne nazwy.
- Monitoruj użycie przestrzeni dyskowej, aby uniknąć problemów z brakiem miejsca.