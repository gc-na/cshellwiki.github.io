# [Linux] C Shell (csh) fc <Użycie: edytowanie i ponowne wykonywanie poleceń>

## Overview
Polecenie `fc` w powłoce C Shell (csh) służy do edytowania i ponownego wykonywania wcześniej wprowadzonych poleceń. Umożliwia użytkownikom przeglądanie historii poleceń oraz ich modyfikację przed ponownym uruchomieniem.

## Usage
Podstawowa składnia polecenia `fc` wygląda następująco:

```csh
fc [opcje] [argumenty]
```

## Common Options
- `-l`: Wyświetla listę ostatnich poleceń z historii.
- `-s`: Wykonuje polecenie bez jego edytowania.
- `-n`: Nie wyświetla numerów poleceń w liście.

## Common Examples
1. **Wyświetlenie ostatnich poleceń**:
   ```csh
   fc -l
   ```

2. **Edytowanie konkretnego polecenia**:
   ```csh
   fc 10
   ```
   (gdzie `10` to numer polecenia w historii)

3. **Wykonanie ostatniego polecenia bez edytowania**:
   ```csh
   fc -s
   ```

4. **Wyświetlenie poleceń z zakresu**:
   ```csh
   fc -l 5 10
   ```
   (wyświetli polecenia od numeru 5 do 10)

## Tips
- Używaj `fc` regularnie, aby szybko poprawić błędy w ostatnich poleceniach.
- Możesz używać edytora tekstu, aby wprowadzać zmiany w poleceniach, co ułatwia ich modyfikację.
- Zapamiętaj numery poleceń, aby sprawnie korzystać z historii i unikać ponownego wpisywania długich komend.