# [Linux] Bash chown użycie: Zmiana właściciela plików i katalogów

## Overview
Polecenie `chown` w systemie Linux służy do zmiany właściciela i grupy plików oraz katalogów. Umożliwia to administratorom zarządzanie dostępem do zasobów systemowych.

## Usage
Podstawowa składnia polecenia `chown` wygląda następująco:

```bash
chown [opcje] [nowy_właściciel][:nowa_grupa] [plik/katalog]
```

## Common Options
- `-R`: Rekursywnie zmienia właściciela dla wszystkich plików i katalogów w podanym katalogu.
- `-v`: Wyświetla szczegółowe informacje o tym, co zostało zmienione.
- `--reference=plik`: Ustawia właściciela i grupę na podstawie innego pliku.

## Common Examples
1. Zmiana właściciela pliku:
   ```bash
   chown janek plik.txt
   ```

2. Zmiana właściciela i grupy pliku:
   ```bash
   chown janek:admin plik.txt
   ```

3. Rekursywna zmiana właściciela katalogu:
   ```bash
   chown -R janek katalog/
   ```

4. Ustawienie właściciela i grupy na podstawie innego pliku:
   ```bash
   chown --reference=plik_wzorcowy plik_do_zmiany.txt
   ```

## Tips
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do zmiany właściciela plików.
- Używaj opcji `-v`, aby zobaczyć, które pliki zostały zmienione, co może pomóc w diagnostyce.
- Przy używaniu opcji `-R` bądź ostrożny, aby nie zmienić właściciela plików systemowych lub ważnych dla działania aplikacji.