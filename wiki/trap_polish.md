# [Linux] C Shell (csh) trap użycie: Ustawianie pułapek na sygnały

## Overview
Polecenie `trap` w C Shell (csh) służy do przechwytywania sygnałów i wykonywania określonych akcji, gdy te sygnały są odbierane przez skrypt lub sesję powłoki. Dzięki temu można zarządzać zachowaniem skryptów w odpowiedzi na różne zdarzenia, takie jak przerwania użytkownika.

## Usage
Podstawowa składnia polecenia `trap` jest następująca:

```csh
trap [akcja] [sygnał]
```

## Common Options
- `action`: Określa, co ma się wydarzyć, gdy sygnał zostanie odebrany (np. wykonanie innego polecenia lub funkcji).
- `signal`: Określa, który sygnał ma być przechwycony (np. `INT`, `TERM`, `QUIT`).

## Common Examples
1. **Przechwytywanie sygnału przerwania (CTRL+C)**:
   ```csh
   trap 'echo "Przerwanie skryptu"; exit' INT
   ```
   W tym przykładzie, gdy użytkownik naciśnie CTRL+C, skrypt wyświetli komunikat i zakończy działanie.

2. **Czyszczenie plików tymczasowych przed zakończeniem**:
   ```csh
   trap 'rm -f /tmp/tempfile; exit' EXIT
   ```
   Tutaj, przed zakończeniem skryptu, plik tymczasowy zostanie usunięty.

3. **Reagowanie na sygnał zakończenia**:
   ```csh
   trap 'echo "Otrzymano sygnał TERM"; exit' TERM
   ```
   W tym przypadku, gdy skrypt otrzyma sygnał TERM, wyświetli komunikat i zakończy działanie.

## Tips
- Zawsze testuj swoje pułapki w środowisku deweloperskim, aby upewnić się, że działają zgodnie z oczekiwaniami.
- Używaj pułapek do zarządzania zasobami, takimi jak pliki tymczasowe, aby uniknąć ich pozostawiania po zakończeniu skryptu.
- Pamiętaj, że niektóre sygnały mogą być ignorowane przez system, więc sprawdź dokumentację, aby zrozumieć, które sygnały są dostępne do przechwytywania.