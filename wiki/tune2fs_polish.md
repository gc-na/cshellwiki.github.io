# [Linux] C Shell (csh) tune2fs użycie: Narzędzie do dostosowywania systemu plików ext2/ext3/ext4

## Overview
Polecenie `tune2fs` służy do modyfikacji parametrów systemu plików ext2, ext3 i ext4. Umożliwia użytkownikom dostosowanie różnych opcji systemu plików, takich jak liczba bloków, rozmiar bloku oraz inne ustawienia, które mogą wpłynąć na wydajność i zachowanie systemu plików.

## Usage
Podstawowa składnia polecenia `tune2fs` jest następująca:

```bash
tune2fs [opcje] [argumenty]
```

## Common Options
- `-c <liczba>`: Ustawia maksymalną liczbę montowań przed sprawdzeniem systemu plików.
- `-i <czas>`: Ustawia maksymalny czas między sprawdzeniami systemu plików.
- `-O <opcje>`: Włącza określone opcje systemu plików.
- `-L <nazwa>`: Ustawia etykietę systemu plików.
- `-e <typ>`: Ustawia domyślny typ błędu dla systemu plików.

## Common Examples
1. Ustawienie maksymalnej liczby montowań przed sprawdzeniem systemu plików na 20:
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

2. Ustawienie maksymalnego czasu między sprawdzeniami systemu plików na 30 dni:
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. Włączenie opcji "dir_index" w systemie plików:
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

4. Ustawienie etykiety systemu plików na "MojaEtykieta":
   ```bash
   tune2fs -L MojaEtykieta /dev/sda1
   ```

5. Ustawienie domyślnego typu błędu na "panic":
   ```bash
   tune2fs -e panic /dev/sda1
   ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed wprowadzeniem zmian w systemie plików.
- Używaj opcji `-l` do wyświetlenia aktualnych ustawień systemu plików przed ich modyfikacją.
- Upewnij się, że system plików nie jest zamontowany podczas używania `tune2fs`, aby uniknąć problemów z integralnością danych.