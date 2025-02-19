# [Linux] C Shell (csh) screen użycie: zarządzanie sesjami terminalowymi

## Overview
Polecenie `screen` w C Shell (csh) służy do zarządzania sesjami terminalowymi. Umożliwia użytkownikom uruchamianie wielu sesji w jednym oknie terminala oraz łatwe przełączanie się między nimi. Dzięki `screen` można również odłączyć sesję i wznowić ją później, co jest szczególnie przydatne w przypadku długotrwałych zadań.

## Usage
Podstawowa składnia polecenia `screen` jest następująca:

```bash
screen [options] [arguments]
```

## Common Options
- `-S <session_name>`: Umożliwia nadanie nazwy sesji, co ułatwia jej późniejsze odnalezienie.
- `-d -r`: Odłącza sesję, jeśli jest aktywna, a następnie ją wznawia.
- `-list`: Wyświetla listę dostępnych sesji.
- `-q`: Uruchamia `screen` w trybie cichym, bez wyświetlania komunikatów.

## Common Examples
1. **Uruchomienie nowej sesji `screen`:**
   ```bash
   screen
   ```

2. **Uruchomienie sesji z nazwą:**
   ```bash
   screen -S moja_sesja
   ```

3. **Odłączenie od sesji:**
   Naciśnij `Ctrl + A`, a następnie `D`.

4. **Wznawianie odłączonej sesji:**
   ```bash
   screen -r
   ```

5. **Wyświetlenie listy sesji:**
   ```bash
   screen -list
   ```

## Tips
- Używaj nazw sesji, aby łatwiej zarządzać wieloma sesjami.
- Regularnie odłączaj sesje, aby uniknąć ich przypadkowego zamknięcia.
- Zapoznaj się z kombinacjami klawiszy `Ctrl + A`, aby szybko nawigować między sesjami.