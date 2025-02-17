# [Linux] Bash cal <Użycie: wyświetlanie kalendarza>

## Overview
Polecenie `cal` w systemie Linux służy do wyświetlania kalendarza w terminalu. Umożliwia szybki podgląd miesięcy, lat oraz dni tygodnia, co jest przydatne do planowania i organizacji.

## Usage
Podstawowa składnia polecenia `cal` jest następująca:

```bash
cal [opcje] [argumenty]
```

## Common Options
- `-m` : Wyświetla kalendarz w formacie miesięcznym.
- `-y` : Wyświetla kalendarz na bieżący rok.
- `-3` : Wyświetla kalendarz dla bieżącego miesiąca oraz miesiąca poprzedniego i następnego.
- `-j` : Wyświetla numery dni w roku.
- `-A <liczba>` : Wyświetla dodatkowe miesiące po bieżącym.
- `-B <liczba>` : Wyświetla dodatkowe miesiące przed bieżącym.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `cal`:

1. Wyświetlenie kalendarza na bieżący miesiąc:
   ```bash
   cal
   ```

2. Wyświetlenie kalendarza na rok 2023:
   ```bash
   cal 2023
   ```

3. Wyświetlenie kalendarza dla miesiąca grudnia 2023:
   ```bash
   cal 12 2023
   ```

4. Wyświetlenie kalendarza dla bieżącego miesiąca oraz miesiąca poprzedniego i następnego:
   ```bash
   cal -3
   ```

5. Wyświetlenie kalendarza z numerami dni w roku:
   ```bash
   cal -j
   ```

## Tips
- Używaj opcji `-A` i `-B`, aby szybko zobaczyć kalendarz w szerszym kontekście, co może być przydatne przy planowaniu.
- Możesz połączyć różne opcje, aby dostosować wyświetlany kalendarz do swoich potrzeb, np. `cal -m -A 1 -B 1` wyświetli kalendarz w formacie miesięcznym z miesiącem poprzednim i następnym.
- Jeśli często korzystasz z kalendarza, rozważ dodanie aliasu do swojego pliku `.bashrc`, aby przyspieszyć dostęp do najczęściej używanych opcji.