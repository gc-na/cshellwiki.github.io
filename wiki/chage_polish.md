# [Linux] C Shell (csh) chage <Użycie: zarządzanie polityką haseł użytkowników>

## Overview
Polecenie `chage` służy do zarządzania polityką haseł użytkowników w systemie Linux. Umożliwia administratorom systemu ustawienie różnych parametrów dotyczących wygasania haseł, takich jak maksymalny czas ważności hasła, czas powiadomienia o wygasaniu oraz minimalny czas między zmianami haseł.

## Usage
Podstawowa składnia polecenia `chage` jest następująca:

```bash
chage [opcje] [argumenty]
```

## Common Options
- `-l`, `--list`: Wyświetla szczegóły dotyczące polityki haseł dla określonego użytkownika.
- `-m`, `--mindays`: Ustawia minimalną liczbę dni między zmianami hasła.
- `-M`, `--maxdays`: Ustawia maksymalną liczbę dni, po których hasło wygasa.
- `-W`, `--warndays`: Ustawia liczbę dni, po których użytkownik zostanie powiadomiony o wygasaniu hasła.
- `-I`, `--inactive`: Ustawia liczbę dni, po których konto użytkownika stanie się nieaktywne po wygaśnięciu hasła.

## Common Examples
1. Wyświetlenie polityki haseł dla użytkownika `janek`:
   ```bash
   chage -l janek
   ```

2. Ustawienie maksymalnej liczby dni na 90 dni dla użytkownika `ania`:
   ```bash
   chage -M 90 ania
   ```

3. Ustawienie minimalnej liczby dni na 7 dni dla użytkownika `marek`:
   ```bash
   chage -m 7 marek
   ```

4. Ustawienie powiadomienia o wygasaniu hasła na 14 dni dla użytkownika `ewa`:
   ```bash
   chage -W 14 ewa
   ```

5. Ustawienie liczby dni nieaktywności na 30 dni dla użytkownika `krzysztof`:
   ```bash
   chage -I 30 krzysztof
   ```

## Tips
- Regularnie sprawdzaj politykę haseł dla użytkowników, aby zapewnić bezpieczeństwo systemu.
- Używaj opcji `-l`, aby szybko zweryfikować ustawienia haseł przed ich modyfikacją.
- Zawsze informuj użytkowników o zmianach w polityce haseł, aby uniknąć nieporozumień.