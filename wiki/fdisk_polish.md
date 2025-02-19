# [Linux] C Shell (csh) fdisk użycie: zarządzanie partycjami dysku

## Overview
Polecenie `fdisk` służy do zarządzania partycjami dysku w systemach operacyjnych Unix i Linux. Umożliwia użytkownikom tworzenie, usuwanie oraz modyfikowanie partycji na dyskach twardych.

## Usage
Podstawowa składnia polecenia `fdisk` jest następująca:

```csh
fdisk [opcje] [argumenty]
```

## Common Options
- `-l` - Wyświetla listę wszystkich dostępnych dysków i ich partycji.
- `-u` - Używa jednostek cylindrów zamiast sektorów.
- `-n` - Tworzy nową partycję.
- `-d` - Usuwa istniejącą partycję.
- `-p` - Wyświetla aktualną tablicę partycji.

## Common Examples
1. **Wyświetlenie listy partycji na dysku**:
   ```csh
   fdisk -l
   ```

2. **Tworzenie nowej partycji**:
   ```csh
   fdisk /dev/sda
   ```
   Następnie w interaktywnym menu wybierz opcję `n`, aby utworzyć nową partycję.

3. **Usuwanie partycji**:
   ```csh
   fdisk /dev/sda
   ```
   W interaktywnym menu wybierz opcję `d`, aby usunąć partycję.

4. **Wyświetlenie tablicy partycji**:
   ```csh
   fdisk -p /dev/sda
   ```

## Tips
- Zawsze wykonuj kopię zapasową danych przed modyfikowaniem partycji, aby uniknąć utraty danych.
- Używaj opcji `-l`, aby szybko sprawdzić, jakie partycje są dostępne przed dokonaniem jakichkolwiek zmian.
- Upewnij się, że masz odpowiednie uprawnienia (najlepiej jako root), aby używać polecenia `fdisk`.