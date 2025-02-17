# [Linux] Bash set użycie: Ustawianie opcji powłoki

## Overview
Polecenie `set` w Bash służy do ustawiania opcji powłoki oraz zmiennych środowiskowych. Umożliwia użytkownikowi dostosowanie zachowania powłoki, co może być przydatne w różnych sytuacjach, takich jak debugowanie skryptów czy zmiana sposobu interpretacji poleceń.

## Usage
Podstawowa składnia polecenia `set` jest następująca:

```bash
set [options] [arguments]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `set`:

- `-e`: Zatrzymuje skrypt, gdy wystąpi błąd (niezerowy kod wyjścia).
- `-u`: Zgłasza błąd, gdy używana jest niezdefiniowana zmienna.
- `-x`: Włącza tryb debugowania, wyświetlając każdą komendę przed jej wykonaniem.
- `-o`: Umożliwia włączenie lub wyłączenie opcji powłoki, np. `-o noclobber` zapobiega nadpisywaniu plików.

## Common Examples

### Przykład 1: Użycie opcji -e
Zatrzymanie skryptu w przypadku błędu:

```bash
set -e
echo "Ten skrypt zatrzyma się, jeśli wystąpi błąd."
false  # To polecenie zwróci błąd, więc skrypt się zatrzyma.
echo "Ten tekst nie zostanie wyświetlony."
```

### Przykład 2: Użycie opcji -u
Zgłaszanie błędu przy użyciu niezdefiniowanej zmiennej:

```bash
set -u
echo "Wartość zmiennej: $NIEZDEFINIOWANA_ZMIENNA"  # To spowoduje błąd.
```

### Przykład 3: Użycie opcji -x
Włączenie trybu debugowania:

```bash
set -x
echo "To jest przykład trybu debugowania."
set +x  # Wyłączenie trybu debugowania.
```

### Przykład 4: Użycie opcji -o
Zapobieganie nadpisywaniu plików:

```bash
set -o noclobber
echo "Zapisz to do pliku." > plik.txt  # To zadziała.
echo "Nadpisz ten plik." > plik.txt  # To spowoduje błąd.
```

## Tips
- Używaj opcji `-e` w skryptach, aby szybko wykrywać błędy.
- Opcja `-u` jest przydatna w dużych skryptach, aby upewnić się, że wszystkie zmienne są zdefiniowane.
- Tryb debugowania (`-x`) może pomóc w analizie problemów w skryptach, ale pamiętaj, aby go wyłączyć po zakończeniu debugowania, aby nie zaśmiecać wyjścia.
- Możesz używać `set +[option]`, aby wyłączyć wcześniej włączone opcje.