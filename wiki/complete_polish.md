# [Linux] Bash complete użycie: Uzupełnianie poleceń

## Overview
Polecenie `complete` w Bash służy do definiowania, jak uzupełnianie poleceń działa dla określonych komend. Umożliwia to dostosowanie uzupełniania, aby lepiej pasowało do specyficznych potrzeb użytkownika.

## Usage
Podstawowa składnia polecenia `complete` wygląda następująco:

```bash
complete [options] [arguments]
```

## Common Options
- `-o` : Umożliwia dodanie opcji do uzupełniania.
- `-F` : Określa funkcję, która ma być używana do uzupełniania.
- `-A` : Umożliwia uzupełnianie na podstawie typu argumentu, np. plików lub katalogów.

## Common Examples

### Przykład 1: Uzupełnianie dla własnej komendy
Aby dodać uzupełnianie dla komendy `mycmd`, można użyć:

```bash
complete -o nospace mycmd
```

### Przykład 2: Użycie funkcji do uzupełniania
Możesz zdefiniować funkcję, która zwraca listę możliwych argumentów:

```bash
_mycmd_completions() {
    local commands="start stop restart"
    COMPREPLY=( $(compgen -W "$commands" -- "${COMP_WORDS[1]}") )
}
complete -F _mycmd_completions mycmd
```

### Przykład 3: Uzupełnianie plików
Aby umożliwić uzupełnianie plików dla komendy `filecmd`, użyj:

```bash
complete -A file filecmd
```

## Tips
- Zawsze testuj nowe uzupełnienia w terminalu, aby upewnić się, że działają zgodnie z oczekiwaniami.
- Używaj opcji `-o` do modyfikacji zachowania uzupełniania, aby dostosować je do swoich potrzeb.
- Pamiętaj, aby dodać definicje uzupełniania do swojego pliku `.bashrc`, aby były dostępne przy każdym uruchomieniu terminala.