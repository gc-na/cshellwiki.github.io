# [Linux] Bash diff użycie: Porównywanie plików i katalogów

## Overview
Polecenie `diff` służy do porównywania dwóch plików tekstowych lub katalogów, aby zidentyfikować różnice między nimi. Umożliwia to użytkownikom łatwe śledzenie zmian w plikach lub analizowanie różnic w wersjach dokumentów.

## Usage
Podstawowa składnia polecenia `diff` wygląda następująco:

```bash
diff [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `diff`:

- `-u`: Wyświetla różnice w formacie "unified", co jest bardziej czytelne i zawiera kontekst.
- `-c`: Wyświetla różnice w formacie "context", który również pokazuje kontekst zmian.
- `-i`: Ignoruje różnice w wielkości liter.
- `-w`: Ignoruje różnice w białych znakach (spacjach i tabulatorach).
- `-r`: Porównuje katalogi rekurencyjnie.

## Common Examples

### Porównanie dwóch plików
Aby porównać dwa pliki tekstowe, użyj:

```bash
diff plik1.txt plik2.txt
```

### Porównanie z opcją unified
Aby uzyskać różnice w formacie "unified":

```bash
diff -u plik1.txt plik2.txt
```

### Ignorowanie wielkości liter
Aby zignorować różnice w wielkości liter:

```bash
diff -i plik1.txt plik2.txt
```

### Porównanie katalogów
Aby porównać dwa katalogi rekurencyjnie:

```bash
diff -r katalog1/ katalog2/
```

### Porównanie z ignorowaniem białych znaków
Aby zignorować różnice w białych znakach:

```bash
diff -w plik1.txt plik2.txt
```

## Tips
- Używaj opcji `-u` lub `-c`, aby uzyskać bardziej czytelne wyniki, szczególnie przy dużych różnicach.
- Zawsze sprawdzaj różnice w plikach konfiguracyjnych przed ich aktualizacją, aby uniknąć niezamierzonych zmian.
- Możesz przekierować wyniki `diff` do pliku, używając `>`:

```bash
diff plik1.txt plik2.txt > różnice.txt
```

Dzięki tym wskazówkom i przykładom, korzystanie z polecenia `diff` stanie się prostsze i bardziej efektywne.