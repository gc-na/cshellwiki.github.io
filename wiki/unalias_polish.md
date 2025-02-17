# [Linux] Bash unalias użycie: Usuwa aliasy z powłoki

## Overview
Polecenie `unalias` w Bash służy do usuwania aliasów, które zostały wcześniej zdefiniowane w bieżącej sesji powłoki. Dzięki temu można przywrócić domyślne zachowanie poleceń, które zostały zmodyfikowane przez aliasy.

## Usage
Podstawowa składnia polecenia `unalias` wygląda następująco:

```bash
unalias [opcje] [argumenty]
```

## Common Options
- `-a`: Usuwa wszystkie zdefiniowane aliasy.
- `-p`: Wyświetla wszystkie aktualnie zdefiniowane aliasy.

## Common Examples

### Usunięcie pojedynczego aliasu
Aby usunąć konkretny alias, użyj polecenia:

```bash
unalias nazwa_aliasu
```

### Usunięcie wszystkich aliasów
Aby usunąć wszystkie aliasy w bieżącej sesji, użyj opcji `-a`:

```bash
unalias -a
```

### Wyświetlenie wszystkich aliasów
Aby zobaczyć wszystkie aktualnie zdefiniowane aliasy, użyj opcji `-p`:

```bash
unalias -p
```

## Tips
- Zawsze sprawdzaj, jakie aliasy są zdefiniowane w twojej sesji, zanim zdecydujesz się je usunąć.
- Jeśli często korzystasz z aliasów, rozważ dodanie ich do pliku konfiguracyjnego, aby były dostępne w każdej sesji.
- Używaj `unalias` ostrożnie, aby nie usunąć aliasów, które mogą być przydatne w twojej pracy.