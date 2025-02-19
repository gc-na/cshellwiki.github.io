# [Linux] C Shell (csh) resize2fs użycie: Zmiana rozmiaru systemu plików ext2/ext3/ext4

## Przegląd
Polecenie `resize2fs` służy do zmiany rozmiaru systemu plików ext2, ext3 i ext4. Umożliwia powiększanie lub zmniejszanie rozmiaru systemu plików, co jest przydatne w zarządzaniu przestrzenią dyskową.

## Użycie
Podstawowa składnia polecenia `resize2fs` jest następująca:

```bash
resize2fs [opcje] [argumenty]
```

## Częste opcje
- `-f`: Wymusza zmianę rozmiaru systemu plików, nawet jeśli system plików jest uszkodzony.
- `-p`: Wyświetla postęp operacji podczas zmiany rozmiaru.
- `-s`: Zmienia rozmiar systemu plików do rozmiaru określonego w argumentach, ale nie zmienia rozmiaru partycji.

## Częste przykłady
1. **Powiększenie systemu plików do maksymalnego rozmiaru partycji:**
   ```bash
   resize2fs /dev/sda1
   ```

2. **Zmiana rozmiaru systemu plików do konkretnego rozmiaru (np. 20G):**
   ```bash
   resize2fs /dev/sda1 20G
   ```

3. **Wymuszenie zmiany rozmiaru systemu plików:**
   ```bash
   resize2fs -f /dev/sda1
   ```

4. **Wyświetlenie postępu podczas zmiany rozmiaru:**
   ```bash
   resize2fs -p /dev/sda1
   ```

## Wskazówki
- Zawsze wykonuj kopię zapasową danych przed zmianą rozmiaru systemu plików, aby uniknąć utraty danych.
- Upewnij się, że system plików jest odmontowany przed jego zmniejszeniem, aby zapobiec uszkodzeniu danych.
- Sprawdź system plików za pomocą `e2fsck` przed i po zmianie rozmiaru, aby upewnić się, że nie ma błędów.