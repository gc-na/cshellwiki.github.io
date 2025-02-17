# [Linux] Bash ls użycie: wyświetlanie zawartości katalogu

## Overview
Polecenie `ls` służy do wyświetlania zawartości katalogu. Umożliwia użytkownikom przeglądanie plików i podkatalogów w danym folderze, co jest przydatne do zarządzania plikami w systemie.

## Usage
Podstawowa składnia polecenia `ls` wygląda następująco:

```bash
ls [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `ls`:

- `-l`: Wyświetla szczegółowe informacje o plikach, w tym uprawnienia, właściciela, rozmiar i datę modyfikacji.
- `-a`: Pokazuje wszystkie pliki, w tym ukryte (zaczynające się od kropki).
- `-h`: Wyświetla rozmiary plików w formacie czytelnym dla ludzi (np. KB, MB).
- `-R`: Rekursywnie wyświetla zawartość podkatalogów.
- `-t`: Sortuje pliki według daty modyfikacji, najnowsze na górze.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ls`:

1. Wyświetlenie zawartości bieżącego katalogu:
   ```bash
   ls
   ```

2. Wyświetlenie szczegółowych informacji o plikach:
   ```bash
   ls -l
   ```

3. Wyświetlenie wszystkich plików, w tym ukrytych:
   ```bash
   ls -a
   ```

4. Wyświetlenie zawartości katalogu z rozmiarami w formacie czytelnym:
   ```bash
   ls -lh
   ```

5. Rekursywne wyświetlenie zawartości katalogu:
   ```bash
   ls -R
   ```

6. Sortowanie plików według daty modyfikacji:
   ```bash
   ls -lt
   ```

## Tips
- Używaj opcji `-lh`, aby łatwiej odczytać rozmiary plików.
- Kombinuj opcje, np. `ls -la` wyświetli wszystkie pliki w szczegółowym formacie.
- Pamiętaj, że `ls` domyślnie sortuje pliki alfabetycznie, co może być przydatne w organizacji plików.