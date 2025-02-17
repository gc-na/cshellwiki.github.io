# [Linux] Bash expand użycie: Rozszerzanie tabulatorów na spacje

## Overview
Polecenie `expand` w systemie Linux służy do konwertowania tabulatorów na spacje w plikach tekstowych. Jest to przydatne, gdy chcemy zapewnić spójne formatowanie tekstu, zwłaszcza w plikach, które będą przetwarzane przez inne narzędzia lub wyświetlane w różnych edytorach.

## Usage
Podstawowa składnia polecenia `expand` wygląda następująco:

```bash
expand [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `expand`:

- `-t, --tabs=SPACES` : Ustala liczbę spacji, które mają zastąpić jeden tabulator. Domyślnie jest to 8 spacji.
- `-i, --initial` : Rozszerza tylko tabulatory, które znajdują się na początku wiersza.
- `-h, --help` : Wyświetla pomoc dotyczącą użycia polecenia.
- `-V, --version` : Wyświetla wersję polecenia `expand`.

## Common Examples

### Przykład 1: Podstawowe użycie
Aby rozszerzyć tabulatory w pliku `plik.txt` na spacje, użyj polecenia:

```bash
expand plik.txt
```

### Przykład 2: Ustalenie liczby spacji
Aby zamienić tabulatory na 4 spacje, użyj opcji `-t`:

```bash
expand -t 4 plik.txt
```

### Przykład 3: Rozszerzanie tylko na początku wiersza
Aby rozszerzyć tabulatory tylko na początku każdego wiersza w pliku, użyj opcji `-i`:

```bash
expand -i plik.txt
```

### Przykład 4: Zapisanie wyniku do nowego pliku
Możesz również zapisać wynik do nowego pliku, używając przekierowania:

```bash
expand plik.txt > nowy_plik.txt
```

## Tips
- Zawsze sprawdzaj, jak wygląda plik po rozszerzeniu tabulatorów, aby upewnić się, że formatowanie jest zgodne z oczekiwaniami.
- Używaj opcji `-t`, aby dostosować liczbę spacji do swoich potrzeb, co może być przydatne w różnych projektach.
- Jeśli pracujesz z plikami, które będą edytowane przez różne osoby, rozważ użycie `expand` przed ich udostępnieniem, aby uniknąć problemów z formatowaniem.