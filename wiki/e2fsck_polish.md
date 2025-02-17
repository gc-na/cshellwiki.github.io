# [Linux] Bash e2fsck użycie: Sprawdzanie i naprawa systemów plików ext2/ext3/ext4

## Overview
Polecenie `e2fsck` służy do sprawdzania i naprawy systemów plików w formatach ext2, ext3 oraz ext4. Umożliwia wykrywanie i korygowanie błędów, co jest kluczowe dla utrzymania integralności danych na dysku.

## Usage
Podstawowa składnia polecenia `e2fsck` jest następująca:

```bash
e2fsck [opcje] [argumenty]
```

## Common Options
- `-p`: Automatycznie naprawia błędy bez interakcji z użytkownikiem.
- `-f`: Wymusza sprawdzenie systemu plików, nawet jeśli nie wydaje się to konieczne.
- `-n`: Wykonuje sprawdzenie w trybie tylko do odczytu, nie dokonując żadnych zmian.
- `-y`: Odpowiada "tak" na wszystkie pytania, co oznacza, że wszystkie naprawy zostaną wykonane automatycznie.

## Common Examples
1. Sprawdzenie systemu plików na urządzeniu `/dev/sda1`:
   ```bash
   e2fsck /dev/sda1
   ```

2. Automatyczne naprawienie błędów na systemie plików:
   ```bash
   e2fsck -p /dev/sda1
   ```

3. Wymuszenie sprawdzenia systemu plików:
   ```bash
   e2fsck -f /dev/sda1
   ```

4. Sprawdzenie systemu plików w trybie tylko do odczytu:
   ```bash
   e2fsck -n /dev/sda1
   ```

5. Automatyczne naprawienie wszystkich błędów:
   ```bash
   e2fsck -y /dev/sda1
   ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed użyciem `e2fsck`, aby uniknąć utraty danych w przypadku poważnych błędów.
- Używaj `e2fsck` tylko wtedy, gdy system plików nie jest zamontowany, aby zapobiec dalszym uszkodzeniom.
- Regularne sprawdzanie systemu plików może pomóc w wczesnym wykrywaniu problemów i utrzymaniu zdrowia dysku.