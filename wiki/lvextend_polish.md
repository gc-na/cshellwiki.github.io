# [Linux] Bash lvextend użycie: Zwiększa rozmiar logicznego woluminu

## Overview
Polecenie `lvextend` służy do zwiększania rozmiaru logicznych woluminów w systemach zarządzania pamięcią masową, takich jak LVM (Logical Volume Manager). Umożliwia to elastyczne zarządzanie przestrzenią dyskową, co jest szczególnie przydatne w przypadku rosnących potrzeb dotyczących przechowywania danych.

## Usage
Podstawowa składnia polecenia `lvextend` jest następująca:

```bash
lvextend [opcje] [argumenty]
```

## Common Options
- `-L +rozmiar`: Zwiększa rozmiar woluminu o określoną wartość (np. `+10G`).
- `-l +liczba`: Zwiększa rozmiar woluminu o określoną liczbę jednostek logicznych.
- `-r`: Automatycznie rozszerza system plików po zwiększeniu rozmiaru woluminu.
- `-n`: Umożliwia zmianę nazwy woluminu.

## Common Examples
### Zwiększenie rozmiaru o 10 GB
Aby zwiększyć rozmiar logicznego woluminu o 10 GB, użyj poniższego polecenia:

```bash
lvextend -L +10G /dev/vg1/lv1
```

### Zwiększenie rozmiaru o 5 jednostek logicznych
Aby zwiększyć rozmiar woluminu o 5 jednostek logicznych, wykonaj:

```bash
lvextend -l +5 /dev/vg1/lv1
```

### Zwiększenie rozmiaru z automatycznym rozszerzeniem systemu plików
Aby zwiększyć rozmiar woluminu i jednocześnie automatycznie rozszerzyć system plików, użyj:

```bash
lvextend -r -L +20G /dev/vg1/lv1
```

### Zmiana nazwy woluminu
Aby zmienić nazwę woluminu, użyj:

```bash
lvextend -n nowa_nazwa /dev/vg1/lv1
```

## Tips
- Zawsze upewnij się, że masz wystarczająco dużo wolnego miejsca w grupie woluminów przed zwiększeniem rozmiaru.
- Przed wykonaniem operacji na woluminach, wykonaj kopię zapasową ważnych danych.
- Używaj opcji `-r` z rozwagą, aby uniknąć problemów z systemem plików po rozszerzeniu woluminu.