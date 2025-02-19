# [Linux] C Shell (csh) yum użycie: Zarządzanie pakietami w systemie Linux

## Overview
Polecenie `yum` (Yellowdog Updater, Modified) jest narzędziem do zarządzania pakietami w systemach Linux opartych na RPM (Red Hat Package Manager). Umożliwia instalację, aktualizację i usuwanie oprogramowania oraz zarządzanie repozytoriami.

## Usage
Podstawowa składnia polecenia `yum` jest następująca:

```bash
yum [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `yum`:

- `install`: Instaluje pakiet.
- `remove`: Usuwa pakiet.
- `update`: Aktualizuje zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety w repozytoriach.
- `info`: Wyświetla szczegóły dotyczące pakietu.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `yum`:

1. **Instalacja pakietu:**
   ```bash
   yum install nazwa_pakietu
   ```

2. **Usuwanie pakietu:**
   ```bash
   yum remove nazwa_pakietu
   ```

3. **Aktualizacja wszystkich zainstalowanych pakietów:**
   ```bash
   yum update
   ```

4. **Wyszukiwanie pakietu:**
   ```bash
   yum search nazwa_pakietu
   ```

5. **Wyświetlanie informacji o pakiecie:**
   ```bash
   yum info nazwa_pakietu
   ```

## Tips
- Zawsze sprawdzaj dostępność aktualizacji przed instalacją nowych pakietów, aby uniknąć konfliktów.
- Używaj opcji `-y`, aby automatycznie potwierdzić instalację lub usunięcie pakietów, co może zaoszczędzić czas.
- Regularnie przeglądaj dostępne repozytoria, aby mieć dostęp do najnowszego oprogramowania.