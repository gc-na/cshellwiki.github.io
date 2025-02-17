# [Linux] Bash 7z użycie: Kompresja i dekompresja plików

## Overview
Polecenie `7z` jest narzędziem do kompresji i dekompresji plików, które obsługuje wiele formatów archiwów, takich jak 7z, ZIP, RAR i inne. Jest częścią pakietu p7zip, który jest portem 7-Zip dla systemów Unix.

## Usage
Podstawowa składnia polecenia `7z` jest następująca:

```bash
7z [opcje] [argumenty]
```

## Common Options
- `a` – dodaje pliki do archiwum.
- `x` – wypakowuje pliki z archiwum.
- `l` – wyświetla listę plików w archiwum.
- `d` – usuwa pliki z archiwum.
- `t` – testuje integralność archiwum.
- `e` – wypakowuje pliki do bieżącego katalogu (bez zachowania struktury katalogów).

## Common Examples

### Tworzenie archiwum
Aby skompresować pliki do archiwum 7z, użyj polecenia:

```bash
7z a archiwum.7z plik1.txt plik2.txt
```

### Wypakowywanie archiwum
Aby wypakować archiwum 7z, użyj polecenia:

```bash
7z x archiwum.7z
```

### Wyświetlanie zawartości archiwum
Aby zobaczyć listę plików w archiwum, użyj polecenia:

```bash
7z l archiwum.7z
```

### Usuwanie pliku z archiwum
Aby usunąć plik z archiwum, użyj polecenia:

```bash
7z d archiwum.7z plik1.txt
```

### Testowanie archiwum
Aby przetestować integralność archiwum, użyj polecenia:

```bash
7z t archiwum.7z
```

## Tips
- Używaj opcji `-p` do zabezpieczania archiwów hasłem, co zwiększa bezpieczeństwo danych.
- Regularnie testuj archiwa, aby upewnić się, że nie są uszkodzone.
- Zawsze twórz kopie zapasowe ważnych plików przed ich kompresją lub usuwaniem z archiwum.