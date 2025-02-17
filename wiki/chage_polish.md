# [Linux] Bash chage użycie: Zarządzanie polityką haseł użytkowników

## Overview
Polecenie `chage` służy do zarządzania polityką haseł użytkowników w systemie Linux. Umożliwia administratorom ustawienie różnych parametrów dotyczących wygasania haseł, takich jak maksymalny czas użytkowania hasła, czas powiadomienia przed wygaśnięciem oraz minimalny czas między zmianami haseł.

## Usage
Podstawowa składnia polecenia `chage` jest następująca:

```bash
chage [opcje] [argumenty]
```

## Common Options
- `-l, --list`: Wyświetla informacje o polityce haseł dla danego użytkownika.
- `-m, --mindays`: Ustawia minimalną liczbę dni między zmianami hasła.
- `-M, --maxdays`: Ustawia maksymalną liczbę dni, po których hasło wygasa.
- `-W, --warndays`: Ustawia liczbę dni, w których użytkownik jest powiadamiany przed wygaśnięciem hasła.
- `-I, --inactive`: Ustawia liczbę dni po wygaśnięciu hasła, po których konto staje się nieaktywne.

## Common Examples
1. **Wyświetlenie polityki haseł dla użytkownika:**

   ```bash
   chage -l username
   ```

2. **Ustawienie maksymalnego czasu użytkowania hasła na 90 dni:**

   ```bash
   chage -M 90 username
   ```

3. **Ustawienie minimalnego czasu między zmianami hasła na 7 dni:**

   ```bash
   chage -m 7 username
   ```

4. **Ustawienie powiadomienia o wygaśnięciu hasła na 14 dni:**

   ```bash
   chage -W 14 username
   ```

5. **Ustawienie konta jako nieaktywnego po 30 dniach od wygaśnięcia hasła:**

   ```bash
   chage -I 30 username
   ```

## Tips
- Zawsze sprawdzaj aktualny stan polityki haseł przed wprowadzeniem zmian, używając opcji `-l`.
- Używaj opcji `-m` i `-M` w parze, aby zapewnić, że użytkownicy będą zmuszeni do regularnej zmiany haseł.
- Regularnie przeglądaj i aktualizuj polityki haseł, aby dostosować je do zmieniających się potrzeb bezpieczeństwa w organizacji.