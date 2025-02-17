# [Linux] Bash parted użycie: Zarządzanie partycjami dysku

## Overview
Polecenie `parted` jest narzędziem do zarządzania partycjami dyskowymi w systemach Linux. Umożliwia tworzenie, usuwanie, zmienianie rozmiaru oraz formatowanie partycji, co jest niezbędne do efektywnego zarządzania przestrzenią dyskową.

## Usage
Podstawowa składnia polecenia `parted` wygląda następująco:

```bash
parted [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji w `parted`:

- `-l` – wyświetla listę dostępnych dysków i ich partycji.
- `mklabel` – tworzy nową tablicę partycji.
- `mkpart` – tworzy nową partycję.
- `rm` – usuwa istniejącą partycję.
- `resizepart` – zmienia rozmiar istniejącej partycji.
- `print` – wyświetla szczegóły dotyczące partycji na wybranym dysku.

## Common Examples

### Wyświetlenie listy partycji
Aby zobaczyć wszystkie partycje na dysku, użyj:

```bash
parted -l
```

### Tworzenie nowej tablicy partycji
Aby utworzyć nową tablicę partycji typu GPT na dysku `/dev/sda`, użyj:

```bash
parted /dev/sda mklabel gpt
```

### Tworzenie nowej partycji
Aby utworzyć nową partycję od 1 GB do 5 GB na dysku `/dev/sda`, użyj:

```bash
parted /dev/sda mkpart primary ext4 1GB 5GB
```

### Usuwanie partycji
Aby usunąć partycję numer 1 na dysku `/dev/sda`, użyj:

```bash
parted /dev/sda rm 1
```

### Zmiana rozmiaru partycji
Aby zmienić rozmiar partycji numer 1 na dysku `/dev/sda` do 10 GB, użyj:

```bash
parted /dev/sda resizepart 1 10GB
```

## Tips
- Zawsze wykonuj kopię zapasową ważnych danych przed modyfikacją partycji.
- Używaj opcji `print` przed i po dokonaniu zmian, aby upewnić się, że operacje zostały wykonane poprawnie.
- Pamiętaj, że niektóre operacje mogą wymagać uprawnień administratora, więc użyj `sudo`, jeśli to konieczne.