# [Linux] Bash pwd użycie: wyświetla bieżący katalog roboczy

## Overview
Polecenie `pwd` (print working directory) służy do wyświetlania pełnej ścieżki do bieżącego katalogu roboczego w systemie plików. Jest to przydatne narzędzie, które pozwala użytkownikom zorientować się, w którym katalogu aktualnie pracują.

## Usage
Podstawowa składnia polecenia `pwd` jest następująca:

```
pwd [opcje]
```

## Common Options
- `-L` - wyświetla ścieżkę do katalogu roboczego z symbolicznymi linkami.
- `-P` - wyświetla ścieżkę do katalogu roboczego z rzeczywistymi ścieżkami, omijając symboliczną linki.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `pwd`:

1. Wyświetlenie bieżącego katalogu roboczego:
   ```bash
   pwd
   ```

2. Wyświetlenie bieżącego katalogu roboczego z symbolicznymi linkami:
   ```bash
   pwd -L
   ```

3. Wyświetlenie bieżącego katalogu roboczego z rzeczywistymi ścieżkami:
   ```bash
   pwd -P
   ```

## Tips
- Używaj `pwd` przed wykonywaniem poleceń, które mogą zmieniać katalog roboczy, aby upewnić się, gdzie się znajdujesz.
- Możesz łączyć `pwd` z innymi poleceniami, aby tworzyć skrypty, które wymagają znajomości bieżącej lokalizacji w systemie plików.