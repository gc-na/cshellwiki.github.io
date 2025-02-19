# [Linux] C Shell (csh) nice użycie: Ustawianie priorytetu procesów

## Overview
Polecenie `nice` w powłoce C Shell (csh) służy do uruchamiania procesów z określonym priorytetem. Dzięki temu można kontrolować, jak dużo zasobów systemowych dany proces może wykorzystać w porównaniu do innych procesów działających w systemie.

## Usage
Podstawowa składnia polecenia `nice` jest następująca:

```csh
nice [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `nice`:

- `-n [wartość]`: Ustala wartość priorytetu. Domyślnie wartość wynosi 10, a wartość może wynosić od -20 (najwyższy priorytet) do 19 (najniższy priorytet).
- `-h`: Wyświetla pomoc dotycząca użycia polecenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `nice`:

1. Uruchomienie programu `my_script.sh` z domyślnym priorytetem:
   ```csh
   nice my_script.sh
   ```

2. Uruchomienie programu `my_script.sh` z priorytetem -5:
   ```csh
   nice -n -5 my_script.sh
   ```

3. Uruchomienie programu `my_script.sh` z priorytetem 15:
   ```csh
   nice -n 15 my_script.sh
   ```

4. Sprawdzenie aktualnego priorytetu procesu:
   ```csh
   nice -n 0
   ```

## Tips
- Używaj `nice` do uruchamiania procesów, które nie są krytyczne, aby nie obciążać systemu.
- Pamiętaj, że tylko użytkownik root może ustawić priorytet poniżej 0.
- Monitoruj obciążenie systemu, aby dostosować priorytety procesów w zależności od potrzeb.