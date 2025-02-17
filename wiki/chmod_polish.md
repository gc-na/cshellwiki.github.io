# [Linux] Bash chmod użycie: Zmiana uprawnień do plików i katalogów

## Overview
Polecenie `chmod` (change mode) służy do zmiany uprawnień dostępu do plików i katalogów w systemach Unix i Linux. Umożliwia to kontrolowanie, kto może czytać, pisać lub wykonywać dany plik.

## Usage
Podstawowa składnia polecenia `chmod` jest następująca:

```bash
chmod [opcje] [argumenty]
```

## Common Options
- `-R`: Rekursywnie zmienia uprawnienia dla katalogów i ich zawartości.
- `-v`: Wyświetla szczegółowe informacje o dokonanych zmianach.
- `-c`: Wyświetla informacje tylko o plikach, dla których zmieniono uprawnienia.

## Common Examples
1. **Ustawienie pełnych uprawnień dla właściciela, a tylko do odczytu dla innych:**
   ```bash
   chmod 744 plik.txt
   ```

2. **Dodanie uprawnienia do wykonywania dla wszystkich użytkowników:**
   ```bash
   chmod a+x skrypt.sh
   ```

3. **Rekurencyjna zmiana uprawnień do odczytu i zapisu dla właściciela oraz do odczytu dla grupy i innych:**
   ```bash
   chmod -R 644 katalog/
   ```

4. **Usunięcie uprawnienia do zapisu dla grupy:**
   ```bash
   chmod g-w plik.txt
   ```

## Tips
- Zawsze sprawdzaj aktualne uprawnienia pliku przed ich zmianą za pomocą polecenia `ls -l`.
- Używaj opcji `-v` lub `-c`, aby mieć pewność, że zmiany zostały zastosowane.
- Unikaj nadawania zbyt szerokich uprawnień (np. `777`), aby nie narazić systemu na niebezpieczeństwo.