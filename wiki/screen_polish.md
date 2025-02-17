# [Linux] Bash screen użycie: zarządzanie sesjami terminalowymi

## Overview
Polecenie `screen` w systemie Linux pozwala na zarządzanie sesjami terminalowymi. Umożliwia uruchamianie programów w wirtualnych terminalach, które mogą działać w tle, a użytkownik może do nich wracać w dowolnym momencie. Jest to szczególnie przydatne w przypadku długotrwałych zadań, które nie powinny być przerywane.

## Usage
Podstawowa składnia polecenia `screen` jest następująca:

```
screen [options] [arguments]
```

## Common Options
- `-S <nazwa>`: Umożliwia nadanie nazwy sesji, co ułatwia jej późniejsze odnalezienie.
- `-d -r <nazwa>`: Odłącza sesję, jeśli jest aktywna, i łączy się z nią ponownie.
- `-list`: Wyświetla listę aktywnych sesji.
- `-h <liczba>`: Ustala liczbę linii, które mają być przechowywane w buforze przewijania.

## Common Examples
1. **Uruchomienie nowej sesji screen:**
   ```bash
   screen
   ```

2. **Uruchomienie sesji z nazwą:**
   ```bash
   screen -S moja_sesja
   ```

3. **Odłączenie od sesji:**
   Naciśnij `Ctrl + A`, a następnie `D`.

4. **Powrót do odłączonej sesji:**
   ```bash
   screen -r moja_sesja
   ```

5. **Wyświetlenie listy aktywnych sesji:**
   ```bash
   screen -list
   ```

## Tips
- Używaj nazw sesji, aby łatwiej zarządzać wieloma sesjami.
- Pamiętaj o regularnym odłączaniu sesji, aby uniknąć ich zatykania.
- Możesz używać `screen` w połączeniu z innymi narzędziami, takimi jak `tmux`, aby zwiększyć efektywność pracy w terminalu.