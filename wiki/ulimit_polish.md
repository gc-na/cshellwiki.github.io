# [Linux] C Shell (csh) ulimit użycie: Ustawianie limitów zasobów dla procesów

## Overview
Polecenie `ulimit` w powłoce C Shell (csh) służy do ustawiania i wyświetlania limitów zasobów dla procesów uruchamianych w danej sesji. Dzięki niemu można kontrolować, ile pamięci, czasu procesora i innych zasobów mogą wykorzystać uruchamiane aplikacje.

## Usage
Podstawowa składnia polecenia `ulimit` wygląda następująco:

```csh
ulimit [opcje] [argumenty]
```

## Common Options
- `-a` - Wyświetla wszystkie aktualne limity.
- `-c [rozmiar]` - Ustawia limit rozmiaru pliku zrzutu pamięci.
- `-d [rozmiar]` - Ustawia limit rozmiaru pamięci danych.
- `-f [rozmiar]` - Ustawia limit rozmiaru pliku, który można utworzyć.
- `-l [rozmiar]` - Ustawia limit rozmiaru pamięci, która może być zablokowana w pamięci.
- `-m [rozmiar]` - Ustawia limit rozmiaru pamięci fizycznej.
- `-s [rozmiar]` - Ustawia limit rozmiaru stosu.
- `-t [czas]` - Ustawia limit czasu CPU dla procesu.

## Common Examples
1. **Wyświetlenie wszystkich limitów:**
   ```csh
   ulimit -a
   ```

2. **Ustawienie limitu rozmiaru pliku na 100 MB:**
   ```csh
   ulimit -f 102400
   ```

3. **Ustawienie limitu czasu CPU na 60 sekund:**
   ```csh
   ulimit -t 60
   ```

4. **Ustawienie limitu rozmiaru pamięci danych na 512 MB:**
   ```csh
   ulimit -d 524288
   ```

5. **Wyświetlenie limitu rozmiaru stosu:**
   ```csh
   ulimit -s
   ```

## Tips
- Zawsze sprawdzaj aktualne limity przed uruchomieniem zasobożernych aplikacji, aby uniknąć nieoczekiwanych błędów.
- Ustawienia `ulimit` są lokalne dla sesji powłoki, więc jeśli chcesz, aby były trwałe, dodaj je do swojego pliku konfiguracyjnego powłoki, np. `.cshrc`.
- Używaj opcji `-a` po każdej zmianie, aby upewnić się, że limity zostały poprawnie ustawione.