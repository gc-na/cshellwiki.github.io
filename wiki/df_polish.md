# [Linux] Bash df użycie: Sprawdzenie dostępnej przestrzeni dyskowej

## Overview
Polecenie `df` (disk free) służy do wyświetlania informacji o dostępnej i używanej przestrzeni dyskowej na zamontowanych systemach plików. Dzięki temu użytkownicy mogą łatwo monitorować, ile miejsca pozostało na dyskach.

## Usage
Podstawowa składnia polecenia `df` jest następująca:

```bash
df [opcje] [argumenty]
```

## Common Options
- `-h` – wyświetla rozmiary w formacie czytelnym dla ludzi (np. KB, MB, GB).
- `-T` – pokazuje typ systemu plików.
- `-a` – wyświetla wszystkie systemy plików, w tym te, które są pełne.
- `-i` – pokazuje informacje o inode'ach zamiast przestrzeni dyskowej.

## Common Examples
1. Wyświetlenie dostępnej przestrzeni na wszystkich zamontowanych systemach plików w formacie czytelnym:
   ```bash
   df -h
   ```

2. Sprawdzenie dostępnej przestrzeni na określonym systemie plików:
   ```bash
   df -h /dev/sda1
   ```

3. Wyświetlenie informacji o typach systemów plików:
   ```bash
   df -T
   ```

4. Sprawdzenie informacji o inode'ach:
   ```bash
   df -i
   ```

## Tips
- Używaj opcji `-h`, aby łatwiej interpretować wyniki, zwłaszcza na dużych dyskach.
- Regularnie monitoruj przestrzeń dyskową, aby unikać problemów z brakiem miejsca.
- Możesz użyć polecenia `df` w skryptach, aby automatycznie sprawdzać dostępność przestrzeni dyskowej przed rozpoczęciem dużych operacji zapisu.