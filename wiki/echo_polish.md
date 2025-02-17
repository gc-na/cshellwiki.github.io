# [Linux] Bash echo użycie: Wyświetlanie tekstu na ekranie

## Overview
Polecenie `echo` w Bashu służy do wyświetlania tekstu lub zmiennych na standardowym wyjściu, zazwyczaj w terminalu. Jest to jedno z najczęściej używanych poleceń w skryptach powłoki.

## Usage
Podstawowa składnia polecenia `echo` jest następująca:

```bash
echo [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `echo`:

- `-n`: Nie dodaje nowej linii na końcu wyjścia.
- `-e`: Włącza interpretację sekwencji ucieczki, takich jak `\n` (nowa linia) czy `\t` (tabulacja).
- `-E`: Wyłącza interpretację sekwencji ucieczki (domyślne ustawienie).

## Common Examples
Poniżej przedstawiono kilka praktycznych przykładów użycia polecenia `echo`:

1. Wyświetlenie prostego tekstu:
   ```bash
   echo "Witaj, świecie!"
   ```

2. Wyświetlenie tekstu bez nowej linii:
   ```bash
   echo -n "To jest tekst bez nowej linii."
   ```

3. Użycie sekwencji ucieczki:
   ```bash
   echo -e "Pierwsza linia\nDruga linia"
   ```

4. Wyświetlenie zmiennej:
   ```bash
   imie="Jan"
   echo "Cześć, $imie!"
   ```

5. Użycie tabulacji:
   ```bash
   echo -e "Kolumna1\tKolumna2"
   ```

## Tips
- Używaj opcji `-n`, gdy chcesz kontynuować wyjście w tej samej linii.
- Opcja `-e` jest przydatna, gdy chcesz formatować tekst z nowymi liniami lub tabulacjami.
- Pamiętaj, że w niektórych systemach `echo` może mieć różne domyślne ustawienia, więc zawsze warto sprawdzić dokumentację lokalną.