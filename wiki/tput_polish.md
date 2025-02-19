# [Linux] C Shell (csh) tput: Ustawienia terminala

## Overview
Polecenie `tput` służy do ustawiania właściwości terminala, takich jak kolory, formatowanie tekstu oraz inne atrybuty wyjścia. Umożliwia to dostosowanie wyglądu i zachowania terminala w skryptach i interaktywnych sesjach.

## Usage
Podstawowa składnia polecenia `tput` jest następująca:

```csh
tput [opcje] [argumenty]
```

## Common Options
- `setaf [num]` - Ustawia kolor tekstu (foreground) na kolor o numerze `num`.
- `setab [num]` - Ustawia kolor tła (background) na kolor o numerze `num`.
- `bold` - Ustawia tekst na pogrubiony.
- `clear` - Czyści ekran terminala.
- `cup [x] [y]` - Ustawia kursor w pozycji (x, y).

## Common Examples
- Ustawienie koloru tekstu na czerwony:
  ```csh
  tput setaf 1
  ```
  
- Ustawienie koloru tła na zielony:
  ```csh
  tput setab 2
  ```

- Pogrubienie tekstu:
  ```csh
  tput bold
  ```

- Czyszczenie ekranu terminala:
  ```csh
  tput clear
  ```

- Ustawienie kursora na pozycję (10, 5):
  ```csh
  tput cup 10 5
  ```

## Tips
- Używaj `tput` w skryptach, aby poprawić czytelność i estetykę wyjścia.
- Możesz łączyć różne polecenia `tput`, aby uzyskać bardziej złożone efekty, np. zmieniając kolor i pogrubiając tekst jednocześnie.
- Sprawdź dostępne kolory w swoim terminalu, ponieważ różne terminale mogą obsługiwać różne zestawy kolorów.