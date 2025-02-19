# [Linux] C Shell (csh) e2fsck użycie: Sprawdzanie i naprawa systemów plików ext2/ext3/ext4

## Overview
Polecenie `e2fsck` służy do sprawdzania i naprawy systemów plików ext2, ext3 oraz ext4. Umożliwia wykrywanie i naprawianie błędów w strukturze systemu plików, co jest kluczowe dla utrzymania integralności danych.

## Usage
Podstawowa składnia polecenia `e2fsck` wygląda następująco:

```bash
e2fsck [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `e2fsck`:

- `-p`: Automatycznie naprawia błędy bez interakcji z użytkownikiem.
- `-f`: Wymusza sprawdzenie systemu plików, nawet jeśli wydaje się, że jest w dobrym stanie.
- `-n`: Nie wykonuje żadnych zmian, tylko wyświetla raport o błędach.
- `-y`: Odpowiada "tak" na wszystkie pytania, automatyzując proces naprawy.

## Common Examples
Oto kilka praktycznych przykładów użycia `e2fsck`:

1. Sprawdzenie systemu plików na urządzeniu `/dev/sda1`:

    ```bash
    e2fsck /dev/sda1
    ```

2. Automatyczna naprawa błędów w systemie plików:

    ```bash
    e2fsck -p /dev/sda1
    ```

3. Wymuszenie sprawdzenia systemu plików:

    ```bash
    e2fsck -f /dev/sda1
    ```

4. Sprawdzenie systemu plików bez wprowadzania zmian:

    ```bash
    e2fsck -n /dev/sda1
    ```

5. Automatyczna naprawa z potwierdzeniem na wszystkie pytania:

    ```bash
    e2fsck -y /dev/sda1
    ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed użyciem `e2fsck`, aby uniknąć utraty danych w przypadku poważnych błędów.
- Używaj `e2fsck` tylko na odmontowanych systemach plików, aby zapobiec dalszym uszkodzeniom.
- Regularne sprawdzanie systemu plików może pomóc w wczesnym wykrywaniu problemów i utrzymaniu zdrowia danych.