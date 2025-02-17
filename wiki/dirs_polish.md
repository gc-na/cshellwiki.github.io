# [Linux] Bash dirs użycie: Zarządzanie katalogami w historii

## Overview
Polecenie `dirs` w Bashu służy do wyświetlania listy katalogów w historii bieżącej powłoki. Umożliwia użytkownikom przeglądanie ścieżek katalogów, które były wcześniej używane w sesji terminalowej.

## Usage
Podstawowa składnia polecenia `dirs` jest następująca:

```bash
dirs [options] [arguments]
```

## Common Options
- `-c`: Czyści listę katalogów.
- `-l`: Wyświetla pełne ścieżki katalogów zamiast ich skróconych wersji.
- `-p`: Wyświetla katalogi w formacie, który jest bardziej przyjazny dla skryptów.

## Common Examples
1. **Wyświetlenie bieżącej listy katalogów:**
   ```bash
   dirs
   ```

2. **Wyświetlenie pełnych ścieżek katalogów:**
   ```bash
   dirs -l
   ```

3. **Dodanie nowego katalogu do listy:**
   ```bash
   cd /path/to/new/directory
   dirs
   ```

4. **Czyszczenie listy katalogów:**
   ```bash
   dirs -c
   ```

5. **Wyświetlenie katalogów w formacie przyjaznym dla skryptów:**
   ```bash
   dirs -p
   ```

## Tips
- Używaj `cd` w połączeniu z `dirs`, aby szybko nawigować między katalogami, które były wcześniej używane.
- Regularnie sprawdzaj listę katalogów, aby mieć lepszą orientację w swojej historii nawigacji.
- Pamiętaj, że `dirs` działa tylko w powłoce Bash i nie jest dostępne w innych powłokach, takich jak sh czy zsh.