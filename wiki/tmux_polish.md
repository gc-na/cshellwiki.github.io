# [Linux] Bash tmux użycie: zarządzanie sesjami terminalowymi

## Przegląd
`tmux` to terminalowy multiplexer, który pozwala na tworzenie, zarządzanie i przełączanie się między wieloma sesjami terminalowymi w jednym oknie. Dzięki niemu można łatwo organizować pracę w terminalu, dzielić okna na panele oraz utrzymywać sesje aktywne nawet po rozłączeniu.

## Użycie
Podstawowa składnia polecenia `tmux` jest następująca:

```bash
tmux [opcje] [argumenty]
```

## Częste opcje
- `new`: Tworzy nową sesję.
- `attach`: Dołącza do istniejącej sesji.
- `list-sessions`: Wyświetla listę aktywnych sesji.
- `kill-session`: Zamyka określoną sesję.
- `split-window`: Dzieli okno na dwa panele.

## Przykłady
1. **Tworzenie nowej sesji:**
   ```bash
   tmux new -s moja_sesja
   ```

2. **Dołączanie do istniejącej sesji:**
   ```bash
   tmux attach -t moja_sesja
   ```

3. **Wyświetlanie listy sesji:**
   ```bash
   tmux list-sessions
   ```

4. **Zamykanie sesji:**
   ```bash
   tmux kill-session -t moja_sesja
   ```

5. **Dzielnie okna na panele:**
   ```bash
   tmux split-window -h
   ```

## Wskazówki
- Używaj skrótów klawiszowych `Ctrl+b` jako prefiksu do wydawania poleceń `tmux`, co znacznie przyspiesza pracę.
- Regularnie zapisuj sesje, aby uniknąć utraty danych w przypadku nagłego zamknięcia terminala.
- Eksperymentuj z różnymi układami paneli, aby dostosować środowisko pracy do swoich potrzeb.