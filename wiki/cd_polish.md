# [Linux] C Shell (csh) cd użycie: Zmiana katalogu roboczego

## Overview
Polecenie `cd` (change directory) w C Shell (csh) służy do zmiany bieżącego katalogu roboczego. Umożliwia użytkownikom nawigację po systemie plików, co jest kluczowe dla wykonywania różnych operacji na plikach i katalogach.

## Usage
Podstawowa składnia polecenia `cd` jest następująca:

```csh
cd [opcje] [argumenty]
```

## Common Options
- `-` : Przechodzi do poprzedniego katalogu.
- `~` : Przechodzi do katalogu domowego użytkownika.
- `..` : Przechodzi do katalogu nadrzędnego.

## Common Examples
1. Przejdź do katalogu domowego:
   ```csh
   cd ~
   ```

2. Przejdź do katalogu nadrzędnego:
   ```csh
   cd ..
   ```

3. Przejdź do konkretnego katalogu (np. do katalogu "Dokumenty"):
   ```csh
   cd Dokumenty
   ```

4. Przejdź do poprzedniego katalogu:
   ```csh
   cd -
   ```

## Tips
- Używaj `cd ~` aby szybko wrócić do katalogu domowego.
- Możesz używać `cd ..` wielokrotnie, aby przejść do wyższych poziomów w hierarchii katalogów.
- Zawsze sprawdzaj bieżący katalog roboczy za pomocą polecenia `pwd`, aby upewnić się, że jesteś w odpowiednim miejscu.