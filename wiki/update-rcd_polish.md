# [Linux] Bash update-rc.d użycie: Zarządzanie skryptami startowymi

## Overview
Polecenie `update-rc.d` służy do zarządzania skryptami startowymi w systemach opartych na Debianie. Umożliwia dodawanie, usuwanie lub aktualizowanie skryptów, które są uruchamiane podczas startu systemu.

## Usage
Podstawowa składnia polecenia `update-rc.d` wygląda następująco:

```bash
update-rc.d [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `update-rc.d`:

- `defaults` - Ustawia domyślne poziomy uruchamiania dla skryptu.
- `remove` - Usuwa skrypt z poziomów uruchamiania.
- `enable` - Włącza skrypt w określonych poziomach uruchamiania.
- `disable` - Wyłącza skrypt w określonych poziomach uruchamiania.

## Common Examples
Oto kilka praktycznych przykładów użycia `update-rc.d`:

1. **Dodanie skryptu do uruchamiania:**

```bash
sudo update-rc.d myscript defaults
```

2. **Usunięcie skryptu z uruchamiania:**

```bash
sudo update-rc.d myscript remove
```

3. **Włączenie skryptu w określonych poziomach uruchamiania:**

```bash
sudo update-rc.d myscript enable
```

4. **Wyłączenie skryptu w określonych poziomach uruchamiania:**

```bash
sudo update-rc.d myscript disable
```

## Tips
- Zawsze sprawdzaj, czy skrypt startowy jest poprawnie napisany, aby uniknąć problemów podczas uruchamiania systemu.
- Używaj opcji `remove` z rozwagą, ponieważ usunięcie skryptu może uniemożliwić uruchomienie niektórych usług.
- Regularnie przeglądaj skrypty startowe, aby upewnić się, że są aktualne i niepotrzebne skrypty są usuwane.