# [Linux] C Shell (csh) vipw użycie: Edytowanie pliku haseł

## Overview
Polecenie `vipw` służy do bezpiecznego edytowania pliku haseł systemowych. Umożliwia użytkownikom modyfikację pliku `/etc/passwd` oraz `/etc/shadow` w sposób, który minimalizuje ryzyko uszkodzenia tych plików.

## Usage
Podstawowa składnia polecenia `vipw` wygląda następująco:

```csh
vipw [opcje]
```

## Common Options
- `-s` : Edytuje plik `/etc/shadow` zamiast `/etc/passwd`.
- `-l` : Używa edytora w trybie blokady, co zapobiega równoczesnemu edytowaniu przez wielu użytkowników.

## Common Examples
1. Aby edytować plik haseł:
   ```csh
   vipw
   ```

2. Aby edytować plik haseł z użyciem opcji blokady:
   ```csh
   vipw -l
   ```

3. Aby edytować plik haseł systemowych:
   ```csh
   vipw -s
   ```

## Tips
- Zawsze wykonuj kopię zapasową plików haseł przed ich edytowaniem, aby uniknąć utraty danych.
- Używaj opcji blokady, aby zapewnić, że tylko jeden użytkownik edytuje plik w danym momencie.
- Sprawdzaj poprawność wprowadzonych zmian przed zapisaniem pliku, aby uniknąć problemów z logowaniem użytkowników.