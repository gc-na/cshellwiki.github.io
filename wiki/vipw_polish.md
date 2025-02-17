# [Linux] Bash vipw użycie: Edytowanie pliku haseł

## Overview
Polecenie `vipw` służy do bezpiecznego edytowania pliku haseł systemu. Umożliwia ono modyfikację pliku `/etc/passwd` oraz `/etc/shadow` w sposób, który zapobiega uszkodzeniu tych plików przez jednoczesne edytowanie ich przez wielu użytkowników.

## Usage
Podstawowa składnia polecenia `vipw` jest następująca:

```bash
vipw [opcje]
```

## Common Options
- `-s`: Edytuje plik `/etc/shadow` zamiast `/etc/passwd`.
- `-h`: Wyświetla pomoc dotycząca użycia polecenia.

## Common Examples
1. Edytowanie pliku haseł:
   ```bash
   vipw
   ```

2. Edytowanie pliku haseł z użyciem opcji `-s`:
   ```bash
   vipw -s
   ```

3. Wyświetlenie pomocy:
   ```bash
   vipw -h
   ```

## Tips
- Zawsze używaj `vipw` do edytowania plików haseł, aby uniknąć problemów z równoczesnym dostępem.
- Upewnij się, że masz odpowiednie uprawnienia do edytowania plików haseł.
- Po zakończeniu edytowania, sprawdź poprawność wprowadzonych zmian, aby uniknąć problemów z logowaniem.