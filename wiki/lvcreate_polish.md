# [Linux] Bash lvcreate użycie: Tworzenie logicznych woluminów

## Overview
Polecenie `lvcreate` jest używane do tworzenia nowych logicznych woluminów w systemach opartych na LVM (Logical Volume Manager). Umożliwia elastyczne zarządzanie przestrzenią dyskową, co jest szczególnie przydatne w środowiskach serwerowych.

## Usage
Podstawowa składnia polecenia `lvcreate` wygląda następująco:

```bash
lvcreate [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `lvcreate`:

- `-n, --name <nazwa>`: Umożliwia określenie nazwy nowego woluminu logicznego.
- `-L, --size <rozmiar>`: Umożliwia określenie rozmiaru nowego woluminu logicznego.
- `-l, --extents <liczba>`: Określa liczbę rozszerzeń, które mają być przydzielone.
- `-m, --mirrors <liczba>`: Tworzy lustrzane kopie woluminu logicznego.
- `-C, --clustered`: Tworzy wolumin w trybie klastrowym.

## Common Examples
Oto kilka praktycznych przykładów użycia `lvcreate`:

1. Tworzenie nowego woluminu logicznego o nazwie `moj_wolumin` i rozmiarze 10 GB:
   ```bash
   lvcreate -n moj_wolumin -L 10G nazwa_grupy_woluminów
   ```

2. Tworzenie woluminu logicznego z określoną liczbą rozszerzeń (np. 20):
   ```bash
   lvcreate -n moj_wolumin -l 20 nazwa_grupy_woluminów
   ```

3. Tworzenie lustrzanego woluminu logicznego:
   ```bash
   lvcreate -n moj_wolumin -L 10G -m 1 nazwa_grupy_woluminów
   ```

4. Tworzenie woluminu logicznego w trybie klastrowym:
   ```bash
   lvcreate -C y -n moj_wolumin -L 10G nazwa_grupy_woluminów
   ```

## Tips
- Zawsze sprawdzaj dostępność przestrzeni w grupie woluminów przed utworzeniem nowego woluminu, aby uniknąć błędów.
- Używaj opcji `-m` do tworzenia lustrzanych kopii, aby zwiększyć niezawodność danych.
- Regularnie monitoruj swoje woluminy logiczne, aby upewnić się, że nie przekraczają dostępnej przestrzeni.