# [Linux] Bash popd użycie: Przywracanie katalogu z listy

## Overview
Polecenie `popd` w Bash służy do przywracania katalogu z listy katalogów, które zostały wcześniej zapisane za pomocą polecenia `pushd`. Umożliwia to łatwe przełączanie się między katalogami bez konieczności wpisywania pełnych ścieżek.

## Usage
Podstawowa składnia polecenia `popd` jest następująca:

```bash
popd [options] [arguments]
```

## Common Options
- `-n`: Nie zmienia katalogu roboczego, tylko aktualizuje stos katalogów.
- `+N`: Przechodzi do katalogu na pozycji N w stosie, licząc od zera.
- `-N`: Przechodzi do katalogu na pozycji N w stosie, licząc od końca.

## Common Examples

1. **Przywracanie ostatniego katalogu:**
   ```bash
   popd
   ```

2. **Przywracanie katalogu z określonej pozycji:**
   ```bash
   popd +1
   ```

3. **Przywracanie katalogu z końca stosu:**
   ```bash
   popd -1
   ```

4. **Użycie opcji -n do aktualizacji stosu bez zmiany katalogu:**
   ```bash
   popd -n
   ```

## Tips
- Używaj `pushd` przed `popd`, aby efektywnie zarządzać katalogami.
- Regularnie sprawdzaj zawartość stosu katalogów za pomocą polecenia `dirs`, aby wiedzieć, które katalogi są dostępne do przywrócenia.
- Pamiętaj, że indeksy w `popd` zaczynają się od zera, co może być pomocne przy nawigacji w stosie.