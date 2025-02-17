# [Linux] Bash blkid użycie: Wyświetlanie informacji o systemie plików

## Overview
Polecenie `blkid` służy do wyświetlania informacji o urządzeniach blokowych w systemie Linux. Umożliwia uzyskanie szczegółowych danych, takich jak identyfikatory UUID, typy systemów plików oraz etykiety partycji.

## Usage
Podstawowa składnia polecenia `blkid` jest następująca:

```bash
blkid [opcje] [argumenty]
```

## Common Options
- `-o, --output`: Określa format wyjścia (np. `value`, `full`, `udev`).
- `-s, --match-tag`: Filtruje wyjście na podstawie określonego tagu.
- `-p, --probe`: Wymusza odczytanie informacji o systemie plików.
- `-c, --cache`: Używa lub aktualizuje pamięć podręczną.

## Common Examples
1. Wyświetlenie wszystkich urządzeń blokowych:
   ```bash
   blkid
   ```

2. Wyświetlenie szczegółowych informacji o konkretnym urządzeniu:
   ```bash
   blkid /dev/sda1
   ```

3. Uzyskanie tylko UUID wszystkich urządzeń:
   ```bash
   blkid -o value -s UUID
   ```

4. Filtracja wyników na podstawie tagu:
   ```bash
   blkid -s TYPE
   ```

## Tips
- Używaj opcji `-o value`, aby uzyskać bardziej czytelne wyjście.
- Regularnie aktualizuj pamięć podręczną za pomocą opcji `-c`, aby mieć pewność, że informacje są aktualne.
- Możesz używać `blkid` w skryptach do automatyzacji zadań związanych z zarządzaniem partycjami.