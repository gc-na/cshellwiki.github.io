# [Linux] Bash grep użycie: Wyszukiwanie wzorców w plikach

## Overview
Polecenie `grep` służy do wyszukiwania wzorców w plikach tekstowych. Umożliwia użytkownikom filtrowanie danych i znajdowanie linii, które pasują do podanego wyrażenia regularnego.

## Usage
Podstawowa składnia polecenia `grep` wygląda następująco:

```bash
grep [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `grep`:

- `-i` – ignoruje wielkość liter podczas wyszukiwania.
- `-r` – przeszukuje katalogi rekurencyjnie.
- `-v` – wyświetla linie, które nie pasują do wzorca.
- `-n` – wyświetla numery linii, w których znaleziono dopasowanie.
- `-l` – wyświetla tylko nazwy plików, które zawierają dopasowanie.

## Common Examples
Oto kilka praktycznych przykładów użycia `grep`:

1. Wyszukiwanie słowa "tekst" w pliku `plik.txt`:

    ```bash
    grep "tekst" plik.txt
    ```

2. Wyszukiwanie słowa "tekst" w pliku `plik.txt`, ignorując wielkość liter:

    ```bash
    grep -i "tekst" plik.txt
    ```

3. Wyszukiwanie słowa "tekst" w wszystkich plikach w bieżącym katalogu i podkatalogach:

    ```bash
    grep -r "tekst" .
    ```

4. Wyświetlanie linii, które nie zawierają słowa "tekst":

    ```bash
    grep -v "tekst" plik.txt
    ```

5. Wyszukiwanie słowa "tekst" w pliku `plik.txt` z numerami linii:

    ```bash
    grep -n "tekst" plik.txt
    ```

## Tips
- Używaj opcji `-i`, gdy nie chcesz, aby wielkość liter wpływała na wyniki wyszukiwania.
- Gdy przeszukujesz wiele plików, użyj opcji `-l`, aby szybko uzyskać listę plików zawierających dopasowanie.
- Regularne wyrażenia mogą być potężnym narzędziem w `grep`, więc warto zapoznać się z ich składnią, aby zwiększyć możliwości wyszukiwania.