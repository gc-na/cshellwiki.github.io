# [Linux] Bash fc użycie: Edytowanie i ponowne wykonywanie poleceń

## Overview
Polecenie `fc` w Bashu służy do edytowania i ponownego wykonywania wcześniej wprowadzonych poleceń. Umożliwia użytkownikowi przeglądanie historii poleceń oraz ich modyfikację przed ponownym wykonaniem.

## Usage
Podstawowa składnia polecenia `fc` wygląda następująco:

```bash
fc [opcje] [argumenty]
```

## Common Options
- `-l`: Wyświetla listę poleceń z historii.
- `-s`: Wykonuje polecenie bez otwierania edytora.
- `-n`: Nie wyświetla numerów poleceń w historii.
- `-e`: Określa edytor do użycia (domyślnie jest to edytor ustawiony w zmiennej środowiskowej `EDITOR`).

## Common Examples
1. **Wyświetlenie ostatnich poleceń**:
   ```bash
   fc -l
   ```

2. **Edytowanie ostatniego polecenia**:
   ```bash
   fc
   ```

3. **Wykonanie ostatniego polecenia bez edycji**:
   ```bash
   fc -s
   ```

4. **Wyświetlenie poleceń z określonego zakresu**:
   ```bash
   fc -l 10 20
   ```

5. **Użycie innego edytora do edycji poleceń**:
   ```bash
   fc -e nano
   ```

## Tips
- Użyj `fc -l` regularnie, aby przeglądać historię poleceń i unikać powtarzania tych samych komend.
- Możesz szybko edytować ostatnie polecenie, co pozwala na łatwe wprowadzanie poprawek.
- Zmieniaj edytor, jeśli preferujesz inny niż domyślny, aby dostosować doświadczenie do swoich potrzeb.