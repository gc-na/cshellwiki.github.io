# [Linux] Bash case użycie: Wybór opcji na podstawie wzorca

## Overview
Polecenie `case` w Bashu służy do wykonywania różnych działań w zależności od wartości zmiennej. Umożliwia to łatwe dopasowanie wzorców i wykonanie odpowiednich bloków kodu w zależności od spełnionych warunków.

## Usage
Podstawowa składnia polecenia `case` wygląda następująco:

```bash
case [zmienna] in
    [wzorzec1])
        # kod do wykonania dla wzorca1
        ;;
    [wzorzec2])
        # kod do wykonania dla wzorca2
        ;;
    *)
        # kod do wykonania, gdy żaden wzorzec nie pasuje
        ;;
esac
```

## Common Options
Polecenie `case` nie ma wielu opcji, ale oto kilka istotnych elementów:

- `*)`: Wzorzec domyślny, który zostanie wykonany, jeśli żaden z wcześniejszych wzorców nie pasuje.
- `;;`: Zakończenie bloku kodu dla danego wzorca.

## Common Examples

### Przykład 1: Prosty wybór
```bash
echo "Podaj dzień tygodnia:"
read dzien

case $dzien in
    poniedziałek)
        echo "Dziś jest poniedziałek."
        ;;
    wtorek)
        echo "Dziś jest wtorek."
        ;;
    *)
        echo "Nieznany dzień."
        ;;
esac
```

### Przykład 2: Wybór na podstawie liczby
```bash
echo "Podaj liczbę od 1 do 3:"
read liczba

case $liczba in
    1)
        echo "Wybrałeś 1."
        ;;
    2)
        echo "Wybrałeś 2."
        ;;
    3)
        echo "Wybrałeś 3."
        ;;
    *)
        echo "Liczba poza zakresem."
        ;;
esac
```

### Przykład 3: Wybór z wieloma wzorcami
```bash
echo "Podaj kolor (czerwony, zielony, niebieski):"
read kolor

case $kolor in
    czerwony|różowy)
        echo "Wybrałeś kolor ciepły."
        ;;
    zielony)
        echo "Wybrałeś kolor neutralny."
        ;;
    niebieski|fioletowy)
        echo "Wybrałeś kolor zimny."
        ;;
    *)
        echo "Nieznany kolor."
        ;;
esac
```

## Tips
- Używaj `case` zamiast wielu instrukcji `if`, gdy masz do czynienia z wieloma warunkami, aby poprawić czytelność kodu.
- Zawsze pamiętaj o dodaniu wzorca domyślnego (`*`), aby obsłużyć nieoczekiwane wartości.
- Możesz używać operatorów logicznych, takich jak `|`, aby grupować wzorce, co pozwala na bardziej zwięzłe i zorganizowane kodowanie.