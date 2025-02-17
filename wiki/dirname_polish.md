# [Linux] Bash dirname użycie: Zwraca katalog z pełnej ścieżki

## Overview
Polecenie `dirname` służy do zwracania katalogu z pełnej ścieżki pliku. Umożliwia to łatwe wydobycie części ścieżki, która wskazuje na folder, w którym znajduje się dany plik.

## Usage
Podstawowa składnia polecenia `dirname` jest następująca:

```bash
dirname [opcje] [argumenty]
```

## Common Options
- `-z` – Zwraca wyniki w formacie null-terminated, co jest przydatne w skryptach, które przetwarzają wiele ścieżek.
- `--help` – Wyświetla pomoc dotyczącą użycia polecenia.
- `--version` – Wyświetla wersję polecenia `dirname`.

## Common Examples
1. **Zwracanie katalogu z pełnej ścieżki:**
   ```bash
   dirname /usr/local/bin/script.sh
   ```
   Wynik: `/usr/local/bin`

2. **Zwracanie katalogu z pliku w bieżącym katalogu:**
   ```bash
   dirname ./myfile.txt
   ```
   Wynik: `.`

3. **Użycie z wieloma argumentami:**
   ```bash
   dirname /home/user/docs/report.pdf /home/user/images/photo.jpg
   ```
   Wynik:
   ```
   /home/user/docs
   /home/user/images
   ```

4. **Z użyciem opcji -z:**
   ```bash
   dirname -z /var/log/syslog
   ```
   Wynik: `/var/log` (zakończony znakiem null)

## Tips
- Używaj `dirname` w skryptach, aby dynamicznie uzyskiwać katalogi dla plików, co ułatwia zarządzanie ścieżkami.
- Łącz `dirname` z innymi poleceniami, takimi jak `basename`, aby uzyskać pełną kontrolę nad ścieżkami plików.
- Pamiętaj, że `dirname` zwraca tylko katalog, więc jeśli potrzebujesz pełnej ścieżki, musisz użyć innych poleceń w połączeniu z `dirname`.