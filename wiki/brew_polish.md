# [macOS] Bash brew użycie: zarządzanie pakietami na macOS

## Overview
Polecenie `brew` jest częścią Homebrew, menedżera pakietów dla systemu macOS. Umożliwia łatwe instalowanie, aktualizowanie i zarządzanie oprogramowaniem oraz bibliotekami, które nie są dostępne w standardowym systemie operacyjnym.

## Usage
Podstawowa składnia polecenia `brew` wygląda następująco:

```bash
brew [opcje] [argumenty]
```

## Common Options
- `install`: Instaluje nowy pakiet.
- `uninstall`: Usuwa zainstalowany pakiet.
- `update`: Aktualizuje listę dostępnych pakietów.
- `upgrade`: Aktualizuje wszystkie zainstalowane pakiety do najnowszych wersji.
- `list`: Wyświetla listę zainstalowanych pakietów.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `brew`:

1. **Instalacja pakietu**:
   ```bash
   brew install wget
   ```

2. **Usunięcie pakietu**:
   ```bash
   brew uninstall wget
   ```

3. **Aktualizacja listy pakietów**:
   ```bash
   brew update
   ```

4. **Aktualizacja zainstalowanych pakietów**:
   ```bash
   brew upgrade
   ```

5. **Wyświetlenie zainstalowanych pakietów**:
   ```bash
   brew list
   ```

## Tips
- Regularnie używaj `brew update`, aby mieć najnowsze informacje o dostępnych pakietach.
- Sprawdzaj dostępność aktualizacji dla zainstalowanych pakietów za pomocą `brew upgrade`, aby korzystać z najnowszych funkcji i poprawek.
- Możesz użyć `brew search [nazwa]`, aby znaleźć pakiety, które mogą Cię interesować.
- Zawsze czytaj dokumentację pakietów, aby dowiedzieć się o ich opcjach i sposobach użycia.