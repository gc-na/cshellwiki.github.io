# [Linux] Bash awk użycie: Przetwarzanie tekstu i danych

## Overview
`awk` to potężne narzędzie w Bash, które służy do przetwarzania i analizy tekstu oraz danych. Umożliwia wykonywanie operacji na danych w formacie tekstowym, takich jak pliki CSV, logi czy inne pliki tekstowe. Dzięki swojej składni i możliwościom, `awk` jest często wykorzystywane do filtrowania, przetwarzania i raportowania danych.

## Usage
Podstawowa składnia polecenia `awk` wygląda następująco:

```bash
awk [opcje] [argumenty]
```

## Common Options
- `-F`: Ustawia separator pól (domyślnie jest to spacja).
- `-v`: Umożliwia przekazywanie zmiennych do skryptu `awk`.
- `-f`: Umożliwia załadowanie skryptu `awk` z pliku.
- `-W`: Umożliwia włączenie dodatkowych opcji, takich jak `compat` dla zgodności z wcześniejszymi wersjami.

## Common Examples
1. **Wyświetlenie drugiego pola z pliku:**
   ```bash
   awk '{print $2}' plik.txt
   ```

2. **Użycie separatora (np. przecinek) do przetwarzania pliku CSV:**
   ```bash
   awk -F, '{print $1, $3}' dane.csv
   ```

3. **Filtracja wierszy, które zawierają określony tekst:**
   ```bash
   awk '/szukany_tekst/' plik.txt
   ```

4. **Sumowanie wartości w trzecim polu:**
   ```bash
   awk '{sum += $3} END {print sum}' plik.txt
   ```

5. **Przekazywanie zmiennej do skryptu:**
   ```bash
   awk -v zmienna=10 '{print $1 + zmienna}' plik.txt
   ```

## Tips
- Używaj opcji `-F`, aby dostosować separator pól do formatu danych, z którym pracujesz.
- Zawsze testuj swoje skrypty `awk` na małych próbkach danych, aby upewnić się, że działają zgodnie z oczekiwaniami.
- Wykorzystuj blok `BEGIN` i `END`, aby wykonywać operacje przed i po przetwarzaniu danych.
- Pamiętaj, że `awk` jest wrażliwe na wielkość liter, więc zwracaj uwagę na to, jak piszesz swoje wzorce.