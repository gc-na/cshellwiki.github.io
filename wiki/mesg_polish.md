# [Linux] Bash mesg użycie: Kontrola dostępu do wiadomości

## Overview
Polecenie `mesg` służy do kontrolowania, czy inne użytkownicy mogą wysyłać wiadomości do terminala użytkownika. Umożliwia to zarządzanie prywatnością i dostępnością w systemach wieloużytkownikowych.

## Usage
Podstawowa składnia polecenia `mesg` jest następująca:

```bash
mesg [opcje] [argumenty]
```

## Common Options
- `y` - Zezwala innym użytkownikom na wysyłanie wiadomości do terminala.
- `n` - Blokuje możliwość wysyłania wiadomości przez innych użytkowników.
- `--help` - Wyświetla pomoc dotyczącą użycia polecenia.

## Common Examples
1. **Zezwolenie na wiadomości:**
   Aby zezwolić innym użytkownikom na wysyłanie wiadomości do twojego terminala, użyj polecenia:
   ```bash
   mesg y
   ```

2. **Blokowanie wiadomości:**
   Aby zablokować możliwość wysyłania wiadomości przez innych użytkowników, użyj polecenia:
   ```bash
   mesg n
   ```

3. **Sprawdzenie aktualnego ustawienia:**
   Aby sprawdzić, czy zezwolenie na wiadomości jest włączone czy wyłączone, wystarczy wpisać:
   ```bash
   mesg
   ```

## Tips
- Używaj `mesg n`, gdy pracujesz nad poufnymi informacjami, aby uniknąć zakłóceń.
- Pamiętaj, że zmiana ustawienia `mesg` dotyczy tylko bieżącej sesji terminala. Po wylogowaniu się lub zamknięciu terminala, ustawienia mogą wrócić do domyślnych wartości.
- Możesz dodać polecenie `mesg y` do swojego pliku konfiguracyjnego powłoki, aby automatycznie zezwalać na wiadomości przy każdym uruchomieniu terminala.