# [Linux] Bash bindkey użycie: Przypisywanie skrótów klawiszowych

## Przegląd
Polecenie `bindkey` w Bash służy do przypisywania skrótów klawiszowych do różnych poleceń lub funkcji w interaktywnym środowisku powłoki. Dzięki temu użytkownicy mogą zwiększyć swoją wydajność, korzystając z własnych, dostosowanych skrótów.

## Użycie
Podstawowa składnia polecenia `bindkey` wygląda następująco:

```bash
bindkey [opcje] [argumenty]
```

## Częste opcje
- `-e`: Ustawia tryb emacs.
- `-v`: Ustawia tryb vi.
- `-s`: Przypisuje skrót klawiszowy do ciągu znaków.
- `-d`: Umożliwia wyświetlenie dostępnych skrótów klawiszowych.

## Częste przykłady
Przykład 1: Przypisanie skrótu klawiszowego do polecenia `ls`.

```bash
bindkey -s '^l' 'ls\n'
```

Przykład 2: Ustawienie trybu vi.

```bash
bindkey -v
```

Przykład 3: Wyświetlenie dostępnych skrótów klawiszowych.

```bash
bindkey -d
```

## Wskazówki
- Zawsze testuj nowe skróty klawiszowe, aby upewnić się, że nie kolidują z istniejącymi.
- Używaj `bindkey -e` lub `bindkey -v`, aby przełączać się między trybami edycji, w zależności od preferencji.
- Dokumentuj swoje przypisane skróty, aby łatwiej było je zapamiętać i ponownie użyć w przyszłości.