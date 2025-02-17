# [Linux] Bash hash użycie: Zarządzanie pamięcią podręczną poleceń

## Overview
Polecenie `hash` w Bash służy do zarządzania pamięcią podręczną poleceń. Umożliwia ono przechowywanie lokalizacji poleceń w pamięci podręcznej, co przyspiesza ich późniejsze wywoływanie.

## Usage
Podstawowa składnia polecenia `hash` jest następująca:

```bash
hash [options] [arguments]
```

## Common Options
- `-r`: Opróżnia pamięć podręczną poleceń.
- `-p`: Umożliwia ustawienie konkretnej ścieżki dla danego polecenia.
- `-l`: Wyświetla wszystkie polecenia w pamięci podręcznej.

## Common Examples
1. **Wyświetlenie pamięci podręcznej poleceń**:
   ```bash
   hash
   ```

2. **Opróżnienie pamięci podręcznej**:
   ```bash
   hash -r
   ```

3. **Dodanie polecenia do pamięci podręcznej z określoną ścieżką**:
   ```bash
   hash -p /usr/local/bin/mycommand mycommand
   ```

4. **Wyświetlenie lokalizacji konkretnego polecenia**:
   ```bash
   hash mycommand
   ```

## Tips
- Używaj `hash -r`, gdy zmieniasz lokalizację poleceń, aby upewnić się, że Bash korzysta z najnowszych ścieżek.
- Regularne sprawdzanie pamięci podręcznej może pomóc w identyfikacji nieaktualnych lub niepoprawnych ścieżek.
- Pamiętaj, że `hash` działa tylko w bieżącej sesji powłoki, więc zmiany nie są trwałe po zamknięciu terminala.