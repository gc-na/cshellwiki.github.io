# [Linux] C Shell (csh) renice: Zmiana priorytetu procesów

## Overview
Polecenie `renice` w systemie C Shell (csh) służy do zmiany priorytetu już działających procesów. Umożliwia to użytkownikom dostosowanie, które procesy powinny otrzymywać więcej lub mniej zasobów systemowych.

## Usage
Podstawowa składnia polecenia `renice` wygląda następująco:

```csh
renice [opcje] [argumenty]
```

## Common Options
- `-n` : Umożliwia ustawienie nowego priorytetu.
- `-p` : Określa, że zmiana dotyczy procesu o podanym identyfikatorze PID.
- `-g` : Zmienia priorytet wszystkich procesów w grupie o podanym identyfikatorze GID.

## Common Examples
1. Zmiana priorytetu pojedynczego procesu:
   ```csh
   renice -n 10 -p 1234
   ```
   W tym przykładzie priorytet procesu o PID 1234 zostanie zmieniony na 10.

2. Zmiana priorytetu wielu procesów:
   ```csh
   renice -n -5 -p 1234 5678
   ```
   Tutaj priorytet procesów o PID 1234 i 5678 zostanie zwiększony o 5.

3. Zmiana priorytetu wszystkich procesów w grupie:
   ```csh
   renice -n 15 -g 1000
   ```
   W tym przypadku wszystkie procesy w grupie o GID 1000 otrzymają priorytet 15.

## Tips
- Używaj `renice` z rozwagą, ponieważ zbyt niski priorytet dla krytycznych procesów może spowodować spowolnienie systemu.
- Sprawdź aktualne priorytety procesów za pomocą polecenia `ps` przed dokonaniem zmian.
- Aby zmienić priorytet na wartość wyższą (czyli bardziej preferowaną), użyj wartości ujemnych.