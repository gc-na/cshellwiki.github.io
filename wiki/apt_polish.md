# [Linux] C Shell (csh) apt użycie: Zarządzanie pakietami

## Overview
Polecenie `apt` jest narzędziem do zarządzania pakietami w systemach opartych na Debianie. Umożliwia instalację, aktualizację i usuwanie oprogramowania, a także zarządzanie zależnościami pakietów.

## Usage
Podstawowa składnia polecenia `apt` wygląda następująco:

```csh
apt [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje nowy pakiet.
- `remove`: Usuwa zainstalowany pakiet.
- `update`: Aktualizuje listę dostępnych pakietów.
- `upgrade`: Aktualizuje wszystkie zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety według nazwy lub opisu.

## Common Examples
- Aby zainstalować pakiet, użyj:

```csh
apt install nazwa_pakietu
```

- Aby usunąć pakiet, użyj:

```csh
apt remove nazwa_pakietu
```

- Aby zaktualizować listę pakietów, użyj:

```csh
apt update
```

- Aby zaktualizować wszystkie zainstalowane pakiety, użyj:

```csh
apt upgrade
```

- Aby wyszukać pakiet, użyj:

```csh
apt search fraza
```

## Tips
- Zawsze wykonuj `apt update` przed instalacją lub aktualizacją pakietów, aby mieć najnowsze informacje o dostępnych wersjach.
- Używaj `apt upgrade` regularnie, aby utrzymać system w aktualnym stanie.
- Rozważ użycie `apt autoremove`, aby usunąć nieużywane pakiety, które mogą zajmować miejsce na dysku.