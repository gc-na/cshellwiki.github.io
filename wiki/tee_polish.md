# [Linux] Bash tee użycie: Zapisuje dane do pliku i wyświetla je na standardowym wyjściu

## Overview
Polecenie `tee` w systemie Linux służy do odczytywania danych ze standardowego wejścia i jednoczesnego zapisywania ich do jednego lub więcej plików. Dzięki temu można łatwo monitorować dane, które są przesyłane przez potoki, a jednocześnie zapisywać je do pliku.

## Usage
Podstawowa składnia polecenia `tee` wygląda następująco:

```bash
tee [opcje] [argumenty]
```

## Common Options
- `-a`, `--append`: Dodaje dane do końca pliku zamiast go nadpisywać.
- `-i`, `--ignore-interrupts`: Ignoruje sygnały przerwania.
- `-p`, `--output-error`: Określa, jak traktować błędy zapisu.

## Common Examples

### Przykład 1: Zapis do pliku
Aby zapisać wyjście polecenia do pliku, można użyć:

```bash
echo "Hello, World!" | tee output.txt
```

### Przykład 2: Zapis z dodawaniem
Aby dodać dane do istniejącego pliku, użyj opcji `-a`:

```bash
echo "Nowa linia" | tee -a output.txt
```

### Przykład 3: Zapis do wielu plików
Możesz zapisać dane do kilku plików jednocześnie:

```bash
echo "Dane do wielu plików" | tee file1.txt file2.txt
```

### Przykład 4: Użycie z innymi poleceniami
Możesz użyć `tee` w potoku z innymi poleceniami:

```bash
ps aux | tee processes.txt | grep bash
```

## Tips
- Używaj opcji `-a`, gdy chcesz zachować istniejące dane w pliku i dodać nowe.
- `tee` jest szczególnie przydatne w skryptach, gdzie chcesz monitorować dane wyjściowe, a jednocześnie je zapisywać.
- Pamiętaj, że `tee` zapisuje dane w formacie tekstowym, więc upewnij się, że pliki, do których zapisujesz, są odpowiednie dla tego formatu.