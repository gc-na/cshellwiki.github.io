# [Linux] C Shell (csh) tmux użycie: Zarządzanie sesjami terminala

## Overview
tmux to terminal multiplexer, który pozwala na tworzenie, zarządzanie i przełączanie się między wieloma sesjami terminalowymi w jednym oknie. Umożliwia użytkownikom pracę w wielu powłokach jednocześnie, co zwiększa efektywność i organizację pracy.

## Usage
Podstawowa składnia polecenia tmux jest następująca:

```
tmux [opcje] [argumenty]
```

## Common Options
- `new`: Tworzy nową sesję tmux.
- `attach`: Dołącza do istniejącej sesji.
- `detach`: Odłącza aktualną sesję.
- `list-sessions`: Wyświetla listę aktywnych sesji.
- `kill-session`: Zamyka wskazaną sesję.

## Common Examples
- **Tworzenie nowej sesji:**
  ```bash
  tmux new -s moja_sesja
  ```
  
- **Dołączanie do istniejącej sesji:**
  ```bash
  tmux attach -t moja_sesja
  ```

- **Odłączanie od sesji:**
  Wciśnij `Ctrl + b`, a następnie `d`.

- **Wyświetlanie listy sesji:**
  ```bash
  tmux list-sessions
  ```

- **Zamykanie sesji:**
  ```bash
  tmux kill-session -t moja_sesja
  ```

## Tips
- Używaj skrótów klawiszowych tmux, aby szybko przełączać się między oknami i panelami.
- Zapisuj sesje, aby móc do nich wrócić później, co jest szczególnie przydatne w długoterminowych projektach.
- Eksperymentuj z podziałem okien, aby efektywnie wykorzystać przestrzeń roboczą.