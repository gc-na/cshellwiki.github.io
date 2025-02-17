# [Linux] Bash lsblk Użycie: Wyświetlanie informacji o urządzeniach blokowych

## Overview
Polecenie `lsblk` służy do wyświetlania informacji o urządzeniach blokowych w systemie Linux. Umożliwia użytkownikom przeglądanie struktury dysków oraz partycji, co jest przydatne w zarządzaniu pamięcią masową.

## Usage
Podstawowa składnia polecenia `lsblk` jest następująca:

```bash
lsblk [opcje] [argumenty]
```

## Common Options
- `-a`, `--all`: Wyświetla wszystkie urządzenia, w tym te, które nie mają zamontowanych partycji.
- `-f`, `--fs`: Pokazuje informacje o systemie plików.
- `-l`, `--list`: Wyświetla wyniki w formacie listy.
- `-o`, `--output`: Określa, które kolumny mają być wyświetlane.
- `-p`, `--paths`: Wyświetla pełne ścieżki do urządzeń.

## Common Examples
1. **Wyświetlenie podstawowych informacji o urządzeniach blokowych:**
   ```bash
   lsblk
   ```

2. **Wyświetlenie szczegółowych informacji o systemie plików:**
   ```bash
   lsblk -f
   ```

3. **Wyświetlenie urządzeń w formacie listy:**
   ```bash
   lsblk -l
   ```

4. **Wyświetlenie tylko wybranych kolumn (np. NAME, SIZE, TYPE):**
   ```bash
   lsblk -o NAME,SIZE,TYPE
   ```

5. **Wyświetlenie wszystkich urządzeń, w tym niezamontowanych:**
   ```bash
   lsblk -a
   ```

## Tips
- Używaj opcji `-f`, aby szybko sprawdzić, jakie systemy plików są zainstalowane na urządzeniach.
- Opcja `-o` pozwala na dostosowanie wyjścia do Twoich potrzeb, co może być przydatne w skryptach.
- Regularnie sprawdzaj stan swoich urządzeń blokowych, aby uniknąć problemów z pamięcią masową.