# [Linux] Bash tr <Użycie: zamiana znaków>

`tr` to polecenie w systemie Unix/Linux, które służy do tłumaczenia lub usuwania znaków z danych wejściowych.

## Overview
Polecenie `tr` (translate) jest używane do przekształcania lub usuwania znaków w strumieniu tekstowym. Może być wykorzystywane do konwersji małych liter na wielkie, usuwania określonych znaków oraz wielu innych operacji na tekstach.

## Usage
Podstawowa składnia polecenia `tr` wygląda następująco:

```bash
tr [opcje] [argumenty]
```

## Common Options
- `-d`: Usuwa znaki z danych wejściowych.
- `-s`: Zmienia powtarzające się znaki na pojedynczy znak.
- `-c`: Używa do tłumaczenia znaków, które nie są wymienione w argumentach.

## Common Examples

### Przykład 1: Zamiana małych liter na wielkie
Aby zamienić wszystkie małe litery na wielkie w pliku tekstowym:

```bash
cat plik.txt | tr 'a-z' 'A-Z'
```

### Przykład 2: Usuwanie spacji
Aby usunąć wszystkie spacje z tekstu:

```bash
echo "To jest przykładowy tekst." | tr -d ' '
```

### Przykład 3: Zmiana powtarzających się spacji
Aby zmienić powtarzające się spacje na pojedynczą spację:

```bash
echo "To    jest    tekst    z    wieloma    spacjami." | tr -s ' '
```

### Przykład 4: Usuwanie określonych znaków
Aby usunąć cyfry z tekstu:

```bash
echo "Tekst z cyframi 12345" | tr -d '0-9'
```

## Tips
- Używaj `tr` w połączeniu z innymi poleceniami, takimi jak `cat` lub `echo`, aby przetwarzać dane wejściowe.
- Pamiętaj, że `tr` działa tylko na strumieniach tekstowych, więc upewnij się, że dane wejściowe są w odpowiednim formacie.
- Możesz używać `tr` w skryptach Bash, aby automatyzować procesy przetwarzania tekstu.