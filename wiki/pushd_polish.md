# [Linux] Bash pushd użycie: Przechodzenie między katalogami

## Overview
Polecenie `pushd` w Bash służy do zmiany katalogów, jednocześnie zapisując bieżący katalog na stosie. Umożliwia to łatwe przełączanie się między katalogami bez potrzeby zapamiętywania ich ścieżek.

## Usage
Podstawowa składnia polecenia `pushd` jest następująca:

```bash
pushd [opcje] [argumenty]
```

## Common Options
- `+N`: Przechodzi do katalogu znajdującego się na pozycji N w stosie.
- `-N`: Przechodzi do katalogu znajdującego się na pozycji N w odwrotnej kolejności.
- `-`: Przechodzi do poprzedniego katalogu.

## Common Examples
1. **Przechodzenie do nowego katalogu:**
   ```bash
   pushd /ścieżka/do/katalogu
   ```

2. **Przechodzenie do katalogu i wyświetlanie stosu:**
   ```bash
   pushd /ścieżka/do/katalogu && dirs
   ```

3. **Powrót do poprzedniego katalogu:**
   ```bash
   pushd -
   ```

4. **Przechodzenie do katalogu na pozycji 1 w stosie:**
   ```bash
   pushd +1
   ```

## Tips
- Używaj `dirs`, aby wyświetlić aktualny stan stosu katalogów.
- Pamiętaj, że `pushd` działa w parze z `popd`, które usuwa katalog z góry stosu i przywraca poprzedni.
- Możesz używać `pushd` w skryptach, aby zarządzać katalogami w bardziej zorganizowany sposób.