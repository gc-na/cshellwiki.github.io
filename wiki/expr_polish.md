# [Linux] C Shell (csh) expr użycie: Obliczanie wyrażeń arytmetycznych i logicznych

## Overview
Polecenie `expr` w C Shell (csh) służy do obliczania wyrażeń arytmetycznych i logicznych. Umożliwia wykonywanie podstawowych operacji matematycznych oraz porównań.

## Usage
Podstawowa składnia polecenia `expr` wygląda następująco:

```csh
expr [opcje] [argumenty]
```

## Common Options
- `+` : dodawanie
- `-` : odejmowanie
- `*` : mnożenie
- `/` : dzielenie
- `%` : reszta z dzielenia
- `=` : porównanie równości
- `!=` : porównanie nierówności
- `<` : porównanie mniejsze
- `>` : porównanie większe
- `-eq` : porównanie równości w kontekście liczbowym
- `-ne` : porównanie nierówności w kontekście liczbowym

## Common Examples
1. **Dodawanie dwóch liczb:**
   ```csh
   expr 5 + 3
   ```
   Wynik: `8`

2. **Odejmowanie:**
   ```csh
   expr 10 - 4
   ```
   Wynik: `6`

3. **Mnożenie:**
   ```csh
   expr 7 \* 6
   ```
   Wynik: `42`

4. **Dzielenie:**
   ```csh
   expr 20 / 4
   ```
   Wynik: `5`

5. **Porównanie równości:**
   ```csh
   expr 5 = 5
   ```
   Wynik: `1` (prawda)

6. **Porównanie nierówności:**
   ```csh
   expr 5 != 3
   ```
   Wynik: `1` (prawda)

## Tips
- Pamiętaj, aby używać znaku `\` przed znakiem mnożenia `*`, aby uniknąć konfliktów z powłoką.
- Używaj nawiasów, aby grupować wyrażenia i kontrolować kolejność operacji.
- `expr` zwraca `0` dla fałszywych warunków, co może być użyteczne w skryptach warunkowych.