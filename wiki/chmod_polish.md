# [Linux] C Shell (csh) chmod użycie: Zmiana uprawnień plików i katalogów

## Overview
Polecenie `chmod` w systemie C Shell (csh) służy do zmiany uprawnień dostępu do plików i katalogów. Umożliwia użytkownikom kontrolowanie, kto może czytać, pisać lub wykonywać dany plik.

## Usage
Podstawowa składnia polecenia `chmod` jest następująca:

```csh
chmod [opcje] [argumenty]
```

## Common Options
- `u`: odnosi się do właściciela pliku (user).
- `g`: odnosi się do grupy użytkowników (group).
- `o`: odnosi się do innych użytkowników (others).
- `a`: odnosi się do wszystkich (all).
- `+`: dodaje uprawnienia.
- `-`: usuwa uprawnienia.
- `=`: ustawia dokładne uprawnienia.

## Common Examples
1. **Dodanie uprawnienia do wykonywania dla właściciela pliku:**
   ```csh
   chmod u+x nazwa_pliku
   ```

2. **Usunięcie uprawnienia do pisania dla grupy:**
   ```csh
   chmod g-w nazwa_pliku
   ```

3. **Ustawienie pełnych uprawnień dla właściciela i grupy, a brak uprawnień dla innych:**
   ```csh
   chmod ug=rwx,o= nazwa_pliku
   ```

4. **Dodanie uprawnienia do odczytu dla wszystkich:**
   ```csh
   chmod a+r nazwa_pliku
   ```

## Tips
- Zawsze sprawdzaj aktualne uprawnienia pliku przed ich zmianą, używając polecenia `ls -l`.
- Używaj opcji `-R`, aby zmienić uprawnienia rekurencyjnie w katalogu i jego podkatalogach.
- Zachowaj ostrożność przy nadawaniu uprawnień do wykonywania, aby nie narazić systemu na niebezpieczeństwo.