# [Linux] Bash pvs użycie: Wyświetlanie informacji o woluminach logicznych

## Przegląd
Polecenie `pvs` (Physical Volumes) jest używane w systemach Linux do wyświetlania informacji o fizycznych woluminach w systemie zarządzania woluminami logicznymi (LVM). Umożliwia użytkownikom monitorowanie stanu woluminów oraz ich właściwości, co jest przydatne w zarządzaniu dyskami i przestrzenią dyskową.

## Użycie
Podstawowa składnia polecenia `pvs` jest następująca:

```bash
pvs [opcje] [argumenty]
```

## Często używane opcje
- `-a`, `--all`: Wyświetla wszystkie woluminy, w tym te, które są nieaktywne.
- `-o`, `--options`: Umożliwia określenie, które kolumny mają być wyświetlane.
- `-h`, `--help`: Wyświetla pomoc dotyczącą użycia polecenia.
- `-v`, `--verbose`: Włącza tryb szczegółowy, pokazując więcej informacji.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `pvs`:

1. Wyświetlenie podstawowych informacji o wszystkich fizycznych woluminach:
   ```bash
   pvs
   ```

2. Wyświetlenie wszystkich woluminów, w tym nieaktywnych:
   ```bash
   pvs -a
   ```

3. Wyświetlenie szczegółowych informacji z trybem szczegółowym:
   ```bash
   pvs -v
   ```

4. Wyświetlenie tylko wybranych kolumn, takich jak nazwa i rozmiar:
   ```bash
   pvs -o +pv_size
   ```

## Wskazówki
- Regularnie używaj `pvs`, aby monitorować stan fizycznych woluminów, co pomoże w zarządzaniu przestrzenią dyskową.
- Używaj opcji `-v`, aby uzyskać więcej informacji, szczególnie podczas rozwiązywania problemów z woluminami.
- Zapisuj wyniki polecenia do pliku, aby móc je później analizować:
  ```bash
  pvs > pvs_output.txt
  ```