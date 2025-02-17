# [Linux] Bash fdisk użycie: Narzędzie do zarządzania partycjami dysków

## Overview
Polecenie `fdisk` jest narzędziem służącym do zarządzania partycjami dysków w systemach operacyjnych opartych na jądrze Linux. Umożliwia użytkownikom tworzenie, usuwanie i modyfikowanie partycji na dyskach twardych oraz innych nośnikach danych.

## Usage
Podstawowa składnia polecenia `fdisk` wygląda następująco:

```bash
fdisk [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `fdisk`:

- `-l`: Wyświetla listę wszystkich dostępnych dysków i ich partycji.
- `-u`: Używa jednostek cylindrów zamiast sektorów do wyświetlania informacji o partycjach.
- `-s`: Wyświetla rozmiar określonej partycji.
- `-n`: Tworzy nową partycję.
- `-d`: Usuwa istniejącą partycję.

## Common Examples

### Wyświetlenie listy partycji
Aby zobaczyć wszystkie dostępne partycje na dysku, użyj:

```bash
fdisk -l
```

### Tworzenie nowej partycji
Aby utworzyć nową partycję, uruchom `fdisk` z odpowiednim dyskiem:

```bash
fdisk /dev/sda
```
Następnie wprowadź `n`, aby dodać nową partycję i postępuj zgodnie z instrukcjami.

### Usuwanie partycji
Aby usunąć partycję, uruchom `fdisk` na odpowiednim dysku:

```bash
fdisk /dev/sda
```
Wprowadź `d`, a następnie wybierz numer partycji, którą chcesz usunąć.

### Wyświetlenie rozmiaru partycji
Aby sprawdzić rozmiar konkretnej partycji, użyj:

```bash
fdisk -s /dev/sda1
```

## Tips
- Zawsze wykonuj kopię zapasową danych przed modyfikowaniem partycji, aby uniknąć utraty danych.
- Używaj opcji `-l` przed wprowadzeniem jakichkolwiek zmian, aby upewnić się, że znasz aktualny układ partycji.
- Po zakończeniu pracy z `fdisk`, pamiętaj o uruchomieniu polecenia `partprobe` lub ponownym uruchomieniu systemu, aby zastosować zmiany.