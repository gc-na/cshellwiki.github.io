# [Linux] C Shell (csh) case <Użycie: przetwarzanie warunkowe>

## Overview
Polecenie `case` w C Shell (csh) służy do wykonywania warunkowego przetwarzania w skryptach. Umożliwia to wybór różnych bloków kodu do wykonania w zależności od wartości zmiennej.

## Usage
Podstawowa składnia polecenia `case` jest następująca:

```csh
case [zmienna] in
    [wzorzec1] ) [komendy1];;
    [wzorzec2] ) [komendy2];;
    ...
    * ) [komendy_domyslne];;
esac
```

## Common Options
Polecenie `case` nie ma wielu opcji, ale oto kilka ważnych elementów:

- `in`: Rozpoczyna listę wzorców do porównania.
- `)` : Oddziela wzorzec od komend do wykonania.
- `;;`: Kończy blok komend dla danego wzorca.
- `*`: Wzorzec domyślny, który jest używany, gdy żaden inny wzorzec nie pasuje.

## Common Examples

### Przykład 1: Proste użycie `case`
```csh
set color = "czerwony"
case $color in
    "czerwony" ) echo "Kolor to czerwony";;
    "zielony" ) echo "Kolor to zielony";;
    * ) echo "Nieznany kolor";;
esac
```

### Przykład 2: Użycie `case` z argumentami skryptu
```csh
case $1 in
    start ) echo "Rozpoczynam...";;
    stop ) echo "Zatrzymuję...";;
    restart ) echo "Restartuję...";;
    * ) echo "Nieznana komenda";;
esac
```

### Przykład 3: Sprawdzanie typu pliku
```csh
set file = $1
case $file in
    *.txt ) echo "To jest plik tekstowy";;
    *.jpg ) echo "To jest plik graficzny";;
    * ) echo "Nieznany typ pliku";;
esac
```

## Tips
- Używaj `case` do uproszczenia skomplikowanych instrukcji warunkowych, aby poprawić czytelność skryptu.
- Pamiętaj o dodaniu wzorca domyślnego (`*`), aby obsłużyć nieoczekiwane wartości.
- Testuj różne wzorce, aby upewnić się, że działają zgodnie z oczekiwaniami, szczególnie w przypadku złożonych warunków.