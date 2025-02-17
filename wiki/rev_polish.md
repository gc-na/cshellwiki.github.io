# [Linux] Bash rev: Odwracanie tekstu w wierszu

## Overview
Polecenie `rev` służy do odwracania kolejności znaków w każdym wierszu pliku lub wejściu standardowym. Jest to przydatne narzędzie, gdy potrzebujesz szybko przekształcić tekst w taki sposób, aby znaki w każdym wierszu były wyświetlane w odwrotnej kolejności.

## Usage
Podstawowa składnia polecenia `rev` jest następująca:

```bash
rev [opcje] [argumenty]
```

## Common Options
- `-o, --output=FILE` - Zapisuje wynik do określonego pliku zamiast wyświetlania na standardowym wyjściu.
- `-h, --help` - Wyświetla pomoc dotyczącą użycia polecenia.
- `-V, --version` - Wyświetla wersję programu.

## Common Examples

### Odwracanie tekstu z wejścia standardowego
Możesz użyć `rev` do odwrócenia tekstu wprowadzonego bezpośrednio w terminalu:

```bash
echo "Hello World" | rev
```
Wynik:
```
dlroW olleH
```

### Odwracanie tekstu z pliku
Jeśli masz plik tekstowy, możesz odwrócić jego zawartość:

```bash
rev plik.txt
```

### Zapisanie odwróconego tekstu do nowego pliku
Możesz również zapisać wynik do nowego pliku:

```bash
rev plik.txt > odwrócony_plik.txt
```

### Odwracanie wielu linii
`rev` działa również na wielu liniach tekstu:

```bash
cat plik.txt | rev
```

## Tips
- Używaj `rev` w połączeniu z innymi poleceniami, aby tworzyć potężne potoki przetwarzania tekstu.
- Sprawdź, czy plik, który chcesz odwrócić, nie zawiera nieoczekiwanych znaków, które mogą wpłynąć na wynik.
- Możesz używać `rev` w skryptach powłoki, aby automatyzować procesy przetwarzania tekstu.