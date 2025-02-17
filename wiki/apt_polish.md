# [Linux] Bash apt użycie: zarządzanie pakietami w systemie

## Overview
Polecenie `apt` (Advanced Package Tool) jest narzędziem do zarządzania pakietami w systemach opartych na Debianie, takich jak Ubuntu. Umożliwia instalację, aktualizację i usuwanie oprogramowania z systemu.

## Usage
Podstawowa składnia polecenia `apt` wygląda następująco:

```bash
apt [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `apt`:

- `install`: Instaluje pakiet.
- `remove`: Usuwa pakiet.
- `update`: Aktualizuje listę dostępnych pakietów.
- `upgrade`: Aktualizuje zainstalowane pakiety do najnowszych wersji.
- `search`: Wyszukuje pakiety w repozytoriach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `apt`:

1. **Aktualizacja listy pakietów:**
   ```bash
   sudo apt update
   ```

2. **Instalacja pakietu (np. `curl`):**
   ```bash
   sudo apt install curl
   ```

3. **Usuwanie pakietu (np. `curl`):**
   ```bash
   sudo apt remove curl
   ```

4. **Aktualizacja wszystkich zainstalowanych pakietów:**
   ```bash
   sudo apt upgrade
   ```

5. **Wyszukiwanie pakietu (np. `git`):**
   ```bash
   apt search git
   ```

## Tips
- Zawsze używaj `sudo` przed poleceniem `apt`, aby uzyskać uprawnienia administratora.
- Regularnie wykonuj `apt update` przed instalacją lub aktualizacją pakietów, aby mieć pewność, że pracujesz z najnowszymi informacjami o dostępnych pakietach.
- Możesz użyć `apt list --upgradable`, aby zobaczyć, które pakiety mogą być zaktualizowane.