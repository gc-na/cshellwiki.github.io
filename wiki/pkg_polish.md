# [Linux] Bash pkg użycie: Zarządzanie pakietami oprogramowania

## Overview
Polecenie `pkg` jest narzędziem do zarządzania pakietami, które umożliwia instalację, aktualizację i usuwanie oprogramowania w systemach operacyjnych opartych na Unixie. Ułatwia ono zarządzanie zależnościami oraz utrzymanie systemu w aktualnym stanie.

## Usage
Podstawowa składnia polecenia `pkg` wygląda następująco:

```bash
pkg [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje nowy pakiet.
- `remove`: Usuwa zainstalowany pakiet.
- `update`: Aktualizuje listę dostępnych pakietów.
- `upgrade`: Aktualizuje zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety według nazwy lub opisu.

## Common Examples
1. **Instalacja pakietu:**
   ```bash
   pkg install nazwa_pakietu
   ```

2. **Usuwanie pakietu:**
   ```bash
   pkg remove nazwa_pakietu
   ```

3. **Aktualizacja listy pakietów:**
   ```bash
   pkg update
   ```

4. **Aktualizacja wszystkich zainstalowanych pakietów:**
   ```bash
   pkg upgrade
   ```

5. **Wyszukiwanie pakietu:**
   ```bash
   pkg search fraza
   ```

## Tips
- Regularnie używaj `pkg update`, aby mieć pewność, że masz dostęp do najnowszych wersji pakietów.
- Zawsze sprawdzaj zależności przed instalacją nowego pakietu, aby uniknąć problemów z kompatybilnością.
- Używaj opcji `-y` podczas instalacji lub usuwania pakietów, aby automatycznie potwierdzać operacje, co przyspiesza proces.