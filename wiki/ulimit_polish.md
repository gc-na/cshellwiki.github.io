# [Linux] Bash ulimit użycie: Ustawianie limitów zasobów dla procesów

## Overview
Polecenie `ulimit` w systemie Linux służy do ustawiania lub wyświetlania limitów zasobów, które mogą być używane przez procesy uruchamiane w danej powłoce. Obejmuje to takie zasoby jak pamięć, liczba otwartych plików i czas CPU. Umożliwia to kontrolowanie wykorzystania zasobów przez aplikacje i zapobieganie ich nadmiernemu zużyciu.

## Usage
Podstawowa składnia polecenia `ulimit` jest następująca:

```bash
ulimit [opcje] [argumenty]
```

## Common Options
- `-a`: Wyświetla wszystkie aktualne limity zasobów.
- `-c`: Ustawia limit rozmiaru pliku zrzutu pamięci (core dump).
- `-d`: Ustawia limit rozmiaru pamięci danych.
- `-f`: Ustawia limit rozmiaru pliku, który może być tworzony przez proces.
- `-l`: Ustawia limit rozmiaru pamięci, która może być zablokowana w pamięci.
- `-n`: Ustawia limit liczby otwartych plików.
- `-s`: Ustawia limit rozmiaru stosu.
- `-t`: Ustawia limit czasu CPU w sekundach.

## Common Examples
1. **Wyświetlenie wszystkich limitów zasobów:**
   ```bash
   ulimit -a
   ```

2. **Ustawienie limitu liczby otwartych plików na 1024:**
   ```bash
   ulimit -n 1024
   ```

3. **Ustawienie limitu rozmiaru pliku na 10 MB:**
   ```bash
   ulimit -f 10240
   ```

4. **Ustawienie limitu czasu CPU na 60 sekund:**
   ```bash
   ulimit -t 60
   ```

5. **Ustawienie limitu rozmiaru stosu na 8 MB:**
   ```bash
   ulimit -s 8192
   ```

## Tips
- Używaj `ulimit -a` na początku, aby zobaczyć aktualne limity przed ich modyfikacją.
- Pamiętaj, że zmiany wprowadzone przez `ulimit` są lokalne dla bieżącej powłoki i nie wpływają na inne sesje.
- Zwiększanie limitów zasobów może być konieczne dla aplikacji wymagających dużych zasobów, ale należy to robić ostrożnie, aby uniknąć problemów z wydajnością systemu.