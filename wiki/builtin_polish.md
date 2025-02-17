# [Linux] Bash builtin `builtin`: Wykonywanie poleceń w powłoce

## Overview
Polecenie `builtin` w Bashu pozwala na wykonywanie wbudowanych poleceń powłoki, które są dostępne bezpośrednio w powłoce, zamiast uruchamiania zewnętrznych programów. Umożliwia to korzystanie z funkcji, które są szybkie i efektywne, ponieważ nie wymagają dodatkowego procesu.

## Usage
Podstawowa składnia polecenia `builtin` jest następująca:

```bash
builtin [opcje] [argumenty]
```

## Common Options
- `-n`: Wykonuje polecenie, ale nie zmienia stanu powłoki.
- `-f`: Wykonuje polecenie w trybie "no function", co oznacza, że nie będzie używać funkcji o tej samej nazwie, jeśli taka istnieje.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `builtin`:

### Przykład 1: Użycie `builtin` do wywołania `echo`
```bash
builtin echo "To jest wbudowane polecenie."
```

### Przykład 2: Użycie `builtin` do wywołania `cd`
```bash
builtin cd /home/user
```

### Przykład 3: Użycie `builtin` do wywołania `exit`
```bash
builtin exit 0
```

## Tips
- Używaj `builtin`, gdy chcesz mieć pewność, że wywołujesz wbudowane polecenie, a nie zewnętrzny program o tej samej nazwie.
- Sprawdzaj, czy polecenie, które chcesz wykonać, jest wbudowane, aby uniknąć niepotrzebnych opóźnień związanych z uruchamianiem zewnętrznych procesów.
- `builtin` jest szczególnie przydatne w skryptach, gdzie chcesz mieć pełną kontrolę nad tym, jakie polecenia są wykonywane.