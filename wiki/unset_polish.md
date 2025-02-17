# [Linux] Bash unset użycie: Usuwa zmienne i funkcje

## Overview
Polecenie `unset` w Bash służy do usuwania zmiennych oraz funkcji z bieżącego środowiska powłoki. Dzięki temu można zwolnić pamięć lub zresetować stan zmiennych.

## Usage
Podstawowa składnia polecenia `unset` jest następująca:

```bash
unset [opcje] [argumenty]
```

## Common Options
- `-f`: Usuwa funkcję. 
- `-v`: Usuwa zmienną. (Domyślnie `unset` działa na zmienne, więc ta opcja jest często pomijana.)

## Common Examples

### Usuwanie zmiennej
Aby usunąć zmienną o nazwie `myVar`, użyj polecenia:

```bash
unset myVar
```

### Usuwanie funkcji
Aby usunąć funkcję o nazwie `myFunction`, użyj polecenia:

```bash
unset -f myFunction
```

### Usuwanie wielu zmiennych
Możesz również usunąć kilka zmiennych jednocześnie:

```bash
unset var1 var2 var3
```

### Sprawdzanie, czy zmienna została usunięta
Możesz sprawdzić, czy zmienna została usunięta, używając polecenia `echo`:

```bash
echo $myVar  # Nie wyświetli nic, jeśli zmienna została usunięta
```

## Tips
- Zawsze upewnij się, że zmienna lub funkcja, którą chcesz usunąć, nie jest już potrzebna, aby uniknąć błędów w skryptach.
- Używaj `unset` w skryptach, aby zarządzać pamięcią i unikać niepotrzebnych zmiennych, które mogą prowadzić do nieprzewidywalnych zachowań.
- Pamiętaj, że `unset` nie może usunąć zmiennych wbudowanych powłoki, takich jak `PATH` czy `HOME`.