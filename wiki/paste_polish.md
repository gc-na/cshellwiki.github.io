# [Linux] Bash paste użycie: Łączenie linii z plików

## Overview
Polecenie `paste` służy do łączenia linii z dwóch lub więcej plików w jeden plik, tworząc wiersze, w których zawartość poszczególnych plików jest oddzielona tabulatorami. Jest to przydatne, gdy chcemy zestawić dane z różnych źródeł w jednym widoku.

## Usage
Podstawowa składnia polecenia `paste` jest następująca:

```bash
paste [opcje] [argumenty]
```

## Common Options
- `-d` : Umożliwia określenie separatora, który ma być użyty zamiast domyślnego tabulatora.
- `-s` : Łączy wszystkie linie z jednego pliku w jeden wiersz.
- `-z` : Używa null jako separatora zamiast nowej linii.

## Common Examples

### Łączenie dwóch plików
Aby połączyć dwie kolumny z plików `plik1.txt` i `plik2.txt`, użyj:

```bash
paste plik1.txt plik2.txt
```

### Użycie innego separatora
Jeśli chcesz użyć przecinka jako separatora, możesz to zrobić w ten sposób:

```bash
paste -d ',' plik1.txt plik2.txt
```

### Łączenie linii w jeden wiersz
Aby połączyć wszystkie linie z jednego pliku w jeden wiersz, użyj opcji `-s`:

```bash
paste -s plik1.txt
```

### Użycie null jako separatora
Aby użyć null jako separatora, możesz użyć opcji `-z`:

```bash
paste -z plik1.txt plik2.txt
```

## Tips
- Używaj opcji `-d` do dostosowania separatora, aby lepiej pasował do formatu danych, z którymi pracujesz.
- Pamiętaj, że `paste` działa na podstawie linii, więc upewnij się, że pliki mają odpowiednią liczbę linii, aby uniknąć nieoczekiwanych wyników.
- Możesz łączyć więcej niż dwa pliki, wystarczy dodać je wszystkie jako argumenty.