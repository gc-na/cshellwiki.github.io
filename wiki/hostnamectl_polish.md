# [Linux] Bash hostnamectl użycie: Zarządzanie nazwą hosta i innymi informacjami systemowymi

## Overview
Polecenie `hostnamectl` jest używane do zarządzania nazwą hosta systemu oraz do uzyskiwania informacji o systemie operacyjnym. Umożliwia użytkownikom łatwe wyświetlanie i modyfikowanie ustawień związanych z nazwą hosta, a także dostęp do informacji o wersji systemu i architekturze.

## Usage
Podstawowa składnia polecenia `hostnamectl` jest następująca:

```bash
hostnamectl [opcje] [argumenty]
```

## Common Options
- `set-hostname`: Umożliwia ustawienie nowej nazwy hosta.
- `status`: Wyświetla aktualny status systemu, w tym nazwę hosta i inne informacje.
- `set-icon-name`: Umożliwia ustawienie ikony systemu.
- `set-chassis`: Umożliwia określenie typu obudowy systemu (np. desktop, laptop).
- `set-deployment`: Umożliwia określenie, czy system jest w trybie produkcyjnym czy testowym.

## Common Examples
1. **Wyświetlenie statusu systemu:**
   ```bash
   hostnamectl status
   ```

2. **Ustawienie nowej nazwy hosta:**
   ```bash
   sudo hostnamectl set-hostname nowa-nazwa-hosta
   ```

3. **Ustawienie ikony systemu:**
   ```bash
   sudo hostnamectl set-icon-name ikona-systemu
   ```

4. **Określenie typu obudowy:**
   ```bash
   sudo hostnamectl set-chassis laptop
   ```

5. **Sprawdzenie wersji systemu:**
   ```bash
   hostnamectl
   ```

## Tips
- Używaj polecenia `sudo`, gdy potrzebujesz uprawnień administratora do zmiany nazwy hosta lub innych ustawień.
- Po zmianie nazwy hosta, rozważ ponowne uruchomienie systemu, aby upewnić się, że wszystkie usługi działają poprawnie.
- Regularnie sprawdzaj status systemu, aby być na bieżąco z informacjami o swoim systemie operacyjnym.