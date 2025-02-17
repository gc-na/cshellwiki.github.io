# [Linux] Bash passwd użycie: Zmiana hasła użytkownika

## Overview
Polecenie `passwd` służy do zmiany hasła użytkownika w systemie Linux. Umożliwia użytkownikom aktualizację swoich haseł oraz administratorom zarządzanie hasłami innych użytkowników.

## Usage
Podstawowa składnia polecenia `passwd` jest następująca:

```bash
passwd [opcje] [argumenty]
```

## Common Options
- `-d` : Usuwa hasło użytkownika, co oznacza, że konto staje się dostępne bez hasła.
- `-l` : Blokuje konto użytkownika, uniemożliwiając logowanie.
- `-u` : Odblokowuje konto użytkownika.
- `-e` : Wymusza zmianę hasła przy następnym logowaniu.
- `-S` : Wyświetla status konta użytkownika.

## Common Examples
1. Zmiana hasła dla bieżącego użytkownika:
   ```bash
   passwd
   ```

2. Zmiana hasła dla innego użytkownika (wymaga uprawnień administratora):
   ```bash
   sudo passwd nazwa_użytkownika
   ```

3. Usunięcie hasła użytkownika:
   ```bash
   sudo passwd -d nazwa_użytkownika
   ```

4. Blokowanie konta użytkownika:
   ```bash
   sudo passwd -l nazwa_użytkownika
   ```

5. Wymuszenie zmiany hasła przy następnym logowaniu:
   ```bash
   sudo passwd -e nazwa_użytkownika
   ```

## Tips
- Zawsze używaj silnych haseł, aby zwiększyć bezpieczeństwo konta.
- Regularnie zmieniaj hasła, zwłaszcza na kontach z uprawnieniami administratora.
- Używaj opcji `-S`, aby sprawdzić status konta przed dokonaniem zmian.