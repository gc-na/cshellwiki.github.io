# [Linux] C Shell (csh) vgextend użycie: Rozszerzanie grupy woluminów

## Overview
Polecenie `vgextend` służy do rozszerzania grupy woluminów (VG) w systemie Linux. Umożliwia dodanie nowych fizycznych woluminów (PV) do istniejącej grupy woluminów, co pozwala na zwiększenie dostępnej przestrzeni dyskowej.

## Usage
Podstawowa składnia polecenia `vgextend` jest następująca:

```bash
vgextend [opcje] [argumenty]
```

## Common Options
- `-l, --extents`: Określa liczbę rozszerzeń do dodania.
- `-n, --noheadings`: Wyłącza nagłówki w wyjściu.
- `-v, --verbose`: Włącza tryb szczegółowy, wyświetlając więcej informacji o postępie operacji.

## Common Examples
1. Rozszerzenie grupy woluminów o nowy fizyczny wolumin:
   ```bash
   vgextend myvg /dev/sdb1
   ```

2. Rozszerzenie grupy woluminów o dwa fizyczne woluminy:
   ```bash
   vgextend myvg /dev/sdb1 /dev/sdc1
   ```

3. Użycie opcji szczegółowych, aby zobaczyć więcej informacji podczas rozszerzania:
   ```bash
   vgextend -v myvg /dev/sdb1
   ```

## Tips
- Zawsze upewnij się, że nowe fizyczne woluminy są poprawnie sformatowane i dostępne przed ich dodaniem do grupy woluminów.
- Regularnie sprawdzaj stan grupy woluminów za pomocą polecenia `vgdisplay`, aby monitorować dostępne zasoby.
- Przed wykonaniem operacji na grupach woluminów, wykonaj kopię zapasową ważnych danych, aby uniknąć ich utraty w przypadku błędów.