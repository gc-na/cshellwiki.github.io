# [Linux] Bash mountpoint użycie: Sprawdza, czy katalog jest punktem montowania

## Overview
Polecenie `mountpoint` służy do sprawdzania, czy dany katalog jest punktem montowania. Umożliwia to użytkownikom szybkie zidentyfikowanie, czy określony folder jest używany do montowania systemów plików.

## Usage
Podstawowa składnia polecenia `mountpoint` jest następująca:

```bash
mountpoint [opcje] [argumenty]
```

## Common Options
- `-q`: Cicha operacja, nie wyświetla żadnych komunikatów.
- `-d`: Wyświetla dodatkowe informacje o punkcie montowania.
- `--help`: Wyświetla pomoc dotyczącą użycia polecenia.

## Common Examples
1. Sprawdzenie, czy katalog `/mnt/dysk` jest punktem montowania:

   ```bash
   mountpoint /mnt/dysk
   ```

2. Użycie opcji cichej, aby nie wyświetlać komunikatów:

   ```bash
   mountpoint -q /mnt/dysk
   ```

3. Wyświetlenie dodatkowych informacji o punkcie montowania:

   ```bash
   mountpoint -d /mnt/dysk
   ```

4. Sprawdzenie wielu katalogów jednocześnie:

   ```bash
   mountpoint /mnt/dysk /mnt/usb
   ```

## Tips
- Używaj opcji `-q`, gdy chcesz sprawdzić punkty montowania w skryptach, aby uniknąć zbędnych komunikatów.
- Regularnie sprawdzaj punkty montowania, aby upewnić się, że system plików jest poprawnie zamontowany.
- Możesz użyć `mountpoint` w połączeniu z innymi poleceniami, aby automatyzować zarządzanie systemami plików.