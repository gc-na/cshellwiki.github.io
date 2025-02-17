# [Linux] Bash usermod użycie: Zmiana właściwości użytkownika

## Overview
Polecenie `usermod` w systemie Linux służy do modyfikacji istniejących kont użytkowników. Umożliwia administratorom systemu wprowadzanie zmian w różnych atrybutach konta, takich jak grupa, hasło, czy katalog domowy.

## Usage
Podstawowa składnia polecenia `usermod` wygląda następująco:

```bash
usermod [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji polecenia `usermod`:

- `-aG` – Dodaje użytkownika do dodatkowej grupy bez usuwania go z innych grup.
- `-d` – Zmienia katalog domowy użytkownika.
- `-l` – Zmienia nazwę użytkownika.
- `-p` – Ustawia hasło użytkownika w postaci zaszyfrowanej.
- `-s` – Zmienia powłokę logowania użytkownika.

## Common Examples

1. **Dodanie użytkownika do grupy:**
   Aby dodać użytkownika `janek` do grupy `developers`, użyj polecenia:
   ```bash
   usermod -aG developers janek
   ```

2. **Zmiana katalogu domowego:**
   Aby zmienić katalog domowy użytkownika `ania` na `/home/ania_new`, wykonaj:
   ```bash
   usermod -d /home/ania_new ania
   ```

3. **Zmiana nazwy użytkownika:**
   Aby zmienić nazwę użytkownika z `stary_nick` na `nowy_nick`, użyj:
   ```bash
   usermod -l nowy_nick stary_nick
   ```

4. **Ustawienie hasła:**
   Aby ustawić hasło dla użytkownika `mariusz`, użyj:
   ```bash
   usermod -p $(openssl passwd -1 nowe_haslo) mariusz
   ```

5. **Zmiana powłoki logowania:**
   Aby zmienić powłokę logowania użytkownika `kasia` na `/bin/zsh`, wykonaj:
   ```bash
   usermod -s /bin/zsh kasia
   ```

## Tips
- Zawsze wykonuj polecenie `usermod` z uprawnieniami administratora (np. użyj `sudo`), aby uniknąć problemów z uprawnieniami.
- Przed wprowadzeniem zmian w koncie użytkownika, warto wykonać kopię zapasową plików konfiguracyjnych.
- Używaj opcji `-aG` z rozwagą, aby nie usunąć użytkownika z innych grup, do których już należy.