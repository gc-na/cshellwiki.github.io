# [Linux] Bash tune2fs użycie: Narzędzie do modyfikacji parametrów systemu plików ext2/ext3/ext4

## Overview
Polecenie `tune2fs` jest używane do modyfikacji parametrów systemu plików ext2, ext3 oraz ext4. Umożliwia użytkownikom dostosowanie różnych opcji systemu plików, takich jak liczba bloków, rozmiar bloków, a także ustawienia dotyczące dziennika.

## Usage
Podstawowa składnia polecenia `tune2fs` jest następująca:

```bash
tune2fs [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `tune2fs`:

- `-c <liczba>`: Ustawia maksymalną liczbę montowań przed sprawdzeniem systemu plików.
- `-i <czas>`: Ustawia interwał czasu między sprawdzeniami systemu plików.
- `-m <procent>`: Ustawia procent miejsca na dysku, które ma być zarezerwowane dla użytkownika root.
- `-O <opcja>`: Włącza określoną opcję w systemie plików.
- `-L <etykieta>`: Ustawia etykietę systemu plików.

## Common Examples
Oto kilka praktycznych przykładów użycia `tune2fs`:

1. Ustawienie maksymalnej liczby montowań przed sprawdzeniem systemu plików na 20:
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

2. Ustawienie interwału czasu między sprawdzeniami systemu plików na 30 dni:
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. Zarezerwowanie 5% miejsca na dysku dla użytkownika root:
   ```bash
   tune2fs -m 5 /dev/sda1
   ```

4. Włączenie opcji "dir_index" w systemie plików:
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

5. Ustawienie etykiety systemu plików na "MojaEtykieta":
   ```bash
   tune2fs -L MojaEtykieta /dev/sda1
   ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed wprowadzeniem zmian w systemie plików.
- Używaj opcji `-l` (mała litera L) do wyświetlenia aktualnych ustawień systemu plików przed dokonaniem zmian.
- Upewnij się, że system plików jest odmontowany przed użyciem `tune2fs`, aby uniknąć uszkodzenia danych.