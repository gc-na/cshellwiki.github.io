# [Linux] Bash switch użycie: Przełączanie między różnymi opcjami

## Overview
Polecenie `switch` w Bashu jest używane do przełączania między różnymi opcjami lub przypadkami w skryptach. Umożliwia to wykonanie różnych działań w zależności od wartości zmiennej.

## Usage
Podstawowa składnia polecenia `switch` wygląda następująco:

```bash
switch [opcje] [argumenty]
```

## Common Options
- `-e`: Umożliwia określenie wyrażenia do oceny.
- `-d`: Ustawia domyślną akcję, która ma być wykonana, jeśli żaden przypadek nie pasuje.
- `-h`: Wyświetla pomoc dotycząca użycia polecenia.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `switch`:

### Przykład 1: Prosty switch
```bash
case $1 in
    start)
        echo "Rozpoczynam..."
        ;;
    stop)
        echo "Zatrzymuję..."
        ;;
    *)
        echo "Nieznana opcja."
        ;;
esac
```

### Przykład 2: Switch z domyślną opcją
```bash
case $1 in
    add)
        echo "Dodawanie..."
        ;;
    remove)
        echo "Usuwanie..."
        ;;
    *)
        echo "Proszę podać 'add' lub 'remove'."
        ;;
esac
```

### Przykład 3: Switch z wieloma argumentami
```bash
case $1 in
    hello)
        echo "Cześć!"
        ;;
    goodbye)
        echo "Do widzenia!"
        ;;
    *)
        echo "Nie rozumiem."
        ;;
esac
```

## Tips
- Używaj `case` zamiast `if` w przypadku wielu warunków, aby poprawić czytelność skryptu.
- Pamiętaj o dodaniu `;;` na końcu każdego przypadku, aby zakończyć dany blok.
- Zawsze uwzględniaj przypadek domyślny (`*`), aby obsłużyć nieoczekiwane wartości.