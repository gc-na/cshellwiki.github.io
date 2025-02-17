# [Linux] Bash umask użycie: Ustawianie domyślnych uprawnień plików

## Overview
Polecenie `umask` w systemie Linux służy do ustawiania domyślnych uprawnień dla nowych plików i katalogów. Umożliwia ono kontrolowanie, jakie uprawnienia będą przypisane do tworzonych zasobów, co może być istotne dla bezpieczeństwa systemu.

## Usage
Podstawowa składnia polecenia `umask` jest następująca:

```bash
umask [opcje] [argumenty]
```

## Common Options
- `-S`: Wyświetla umask w formie symbolicznej.
- `-p`: Wyświetla aktualną wartość umask w formacie, który można użyć w skryptach powłoki.

## Common Examples
1. **Wyświetlenie aktualnej wartości umask:**
   ```bash
   umask
   ```

2. **Ustawienie umask na 022 (czyli pliki będą miały uprawnienia 644, a katalogi 755):**
   ```bash
   umask 022
   ```

3. **Ustawienie umask na 077 (czyli pliki będą miały uprawnienia 600, a katalogi 700):**
   ```bash
   umask 077
   ```

4. **Wyświetlenie umask w formie symbolicznej:**
   ```bash
   umask -S
   ```

5. **Ustawienie umask w skrypcie powłoki:**
   ```bash
   #!/bin/bash
   umask 027
   ```

## Tips
- Zawsze sprawdzaj aktualną wartość umask przed tworzeniem nowych plików, aby upewnić się, że mają odpowiednie uprawnienia.
- Używaj umask w skryptach, aby zapewnić, że nowe pliki i katalogi będą miały odpowiednie uprawnienia, co zwiększy bezpieczeństwo.
- Pamiętaj, że umask działa na poziomie użytkownika, więc różni użytkownicy mogą mieć różne ustawienia umask.