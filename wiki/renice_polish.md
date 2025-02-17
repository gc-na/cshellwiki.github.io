# [Linux] Bash renice użycie: Zmiana priorytetu procesów

## Overview
Polecenie `renice` służy do zmiany priorytetu już działających procesów w systemie Linux. Priorytet procesu wpływa na to, jak dużo czasu procesora otrzymuje w porównaniu do innych procesów. Niższy numer priorytetu oznacza wyższy priorytet.

## Usage
Podstawowa składnia polecenia `renice` jest następująca:

```bash
renice [opcje] [wartość priorytetu] [PID]
```

## Common Options
- `-n`, `--priority`: Umożliwia ustawienie nowego priorytetu.
- `-p`, `--pid`: Określa identyfikator procesu (PID), którego priorytet ma być zmieniony.
- `-g`, `--group`: Zmienia priorytet wszystkich procesów w danej grupie.
- `-u`, `--user`: Zmienia priorytet wszystkich procesów uruchomionych przez określonego użytkownika.

## Common Examples
1. Zmiana priorytetu pojedynczego procesu:
   ```bash
   renice -n 10 -p 1234
   ```
   W tym przykładzie priorytet procesu o PID 1234 zostaje ustawiony na 10.

2. Zmiana priorytetu wszystkich procesów użytkownika:
   ```bash
   renice -n 5 -u username
   ```
   Tutaj wszystkie procesy uruchomione przez użytkownika `username` otrzymują priorytet 5.

3. Zmiana priorytetu grupy procesów:
   ```bash
   renice -n -5 -g groupname
   ```
   W tym przypadku wszystkie procesy w grupie `groupname` mają priorytet ustawiony na -5.

## Tips
- Zmiana priorytetu procesów wymaga uprawnień administratora, więc często konieczne jest użycie polecenia `sudo`.
- Używaj wartości priorytetu w zakresie od -20 (najwyższy priorytet) do 19 (najniższy priorytet).
- Regularnie monitoruj priorytety procesów, aby upewnić się, że system działa optymalnie, szczególnie w środowiskach z dużym obciążeniem.