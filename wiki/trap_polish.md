# [Linux] Bash trap użycie: obsługuje sygnały i zdarzenia

## Overview
Polecenie `trap` w Bashu służy do przechwytywania sygnałów i zdarzeń, umożliwiając wykonanie określonych działań, gdy skrypt napotka określony sygnał. Dzięki temu można kontrolować, co się dzieje w momencie, gdy skrypt jest przerywany lub kończony.

## Usage
Podstawowa składnia polecenia `trap` wygląda następująco:

```bash
trap [akcja] [sygnał]
```

Gdzie `akcja` to polecenie do wykonania, a `sygnał` to sygnał, który ma być przechwycony.

## Common Options
- `SIGINT`: Sygnał przerwania (np. Ctrl+C).
- `SIGTERM`: Sygnał zakończenia procesu.
- `EXIT`: Sygnał, który jest wywoływany, gdy skrypt kończy działanie.
- `ERR`: Sygnał, który jest wywoływany, gdy wystąpi błąd w skrypcie.

## Common Examples

### Przykład 1: Obsługa sygnału przerwania
```bash
trap 'echo "Skrypt został przerwany"; exit' SIGINT
while true; do
    echo "Działam..."
    sleep 1
done
```
W tym przykładzie, gdy użytkownik naciśnie Ctrl+C, skrypt wyświetli komunikat i zakończy działanie.

### Przykład 2: Zapis do pliku przy zakończeniu
```bash
trap 'echo "Skrypt zakończony" >> log.txt' EXIT
echo "Rozpoczynam skrypt..."
sleep 5
```
Tutaj, po zakończeniu skryptu, do pliku `log.txt` zostanie dodany komunikat.

### Przykład 3: Obsługa błędów
```bash
trap 'echo "Wystąpił błąd!"' ERR
false  # To polecenie zawsze zwraca błąd
```
W tym przypadku, gdy wystąpi błąd, skrypt wyświetli komunikat o błędzie.

## Tips
- Używaj `trap` do czyszczenia zasobów, takich jak pliki tymczasowe, przed zakończeniem skryptu.
- Zawsze testuj skrypty z `trap`, aby upewnić się, że odpowiednie akcje są wykonywane w przypadku przechwycenia sygnałów.
- Możesz używać wielu sygnałów w jednym poleceniu `trap`, oddzielając je spacjami.