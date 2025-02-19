# [Linux] C Shell (csh) usermod <Użycie: modyfikacja użytkowników>

## Przegląd
Polecenie `usermod` w C Shell (csh) służy do modyfikacji istniejących kont użytkowników w systemie. Umożliwia administratorom systemu wprowadzanie zmian w atrybutach kont, takich jak grupa, hasło, czy katalog domowy.

## Użycie
Podstawowa składnia polecenia `usermod` wygląda następująco:

```csh
usermod [opcje] [argumenty]
```

## Częste opcje
- `-a`: Dodaje użytkownika do dodatkowej grupy.
- `-G`: Określa grupy, do których użytkownik ma być przypisany.
- `-d`: Zmienia katalog domowy użytkownika.
- `-l`: Zmienia nazwę użytkownika.
- `-p`: Ustawia nowe hasło użytkownika.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `usermod`:

1. **Dodanie użytkownika do grupy:**
   ```csh
   usermod -a -G developers janek
   ```

2. **Zmiana katalogu domowego użytkownika:**
   ```csh
   usermod -d /home/janek janek
   ```

3. **Zmiana nazwy użytkownika:**
   ```csh
   usermod -l nowa_nazwa janek
   ```

4. **Ustawienie nowego hasła dla użytkownika:**
   ```csh
   usermod -p nowe_haslo janek
   ```

## Wskazówki
- Upewnij się, że masz odpowiednie uprawnienia administracyjne przed użyciem `usermod`.
- Zawsze wykonuj kopię zapasową danych użytkownika przed wprowadzeniem istotnych zmian.
- Sprawdzaj aktualny stan użytkowników i grup, aby uniknąć niezamierzonych błędów.