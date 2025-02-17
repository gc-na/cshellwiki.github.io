# [Linux] Bash split użycie: Dzieli pliki na mniejsze części

## Overview
Polecenie `split` w systemie Linux służy do dzielenia dużych plików na mniejsze fragmenty. Jest to przydatne, gdy potrzebujesz podzielić plik na mniejsze części, które można łatwiej przesyłać lub przetwarzać.

## Usage
Podstawowa składnia polecenia `split` wygląda następująco:

```bash
split [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `split`:

- `-l NUM` – dzieli plik na części zawierające NUM linii.
- `-b SIZE` – dzieli plik na części o rozmiarze SIZE (np. `1M` dla 1 megabajta).
- `-d` – używa cyfr do nazywania plików wyjściowych zamiast domyślnych liter.
- `--additional-suffix=SUFFIX` – dodaje SUFFIX do nazw plików wyjściowych.

## Common Examples

1. **Podział pliku na części po 1000 linii:**

   ```bash
   split -l 1000 duzy_plik.txt
   ```

2. **Podział pliku na części o rozmiarze 1 MB:**

   ```bash
   split -b 1M duzy_plik.txt
   ```

3. **Podział pliku z użyciem cyfr w nazwach plików:**

   ```bash
   split -d -l 500 duzy_plik.txt
   ```

4. **Podział pliku z dodatkowym sufiksem:**

   ```bash
   split --additional-suffix=.txt -l 2000 duzy_plik.txt czesc_
   ```

## Tips
- Upewnij się, że masz wystarczająco dużo miejsca na dysku, aby pomieścić wszystkie podzielone pliki.
- Możesz użyć polecenia `cat`, aby połączyć podzielone pliki z powrotem w jeden plik.
- Zawsze sprawdzaj, czy podział pliku nie wpłynie na jego integralność, zwłaszcza w przypadku plików binarnych.