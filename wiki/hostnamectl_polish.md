# [Linux] C Shell (csh) hostnamectl użycie: Zmiana i wyświetlanie nazwy hosta

## Przegląd
Polecenie `hostnamectl` jest używane do zarządzania nazwą hosta systemu operacyjnego. Umożliwia użytkownikom wyświetlanie, ustawianie i modyfikowanie nazwy hosta oraz innych informacji o systemie.

## Użycie
Podstawowa składnia polecenia `hostnamectl` jest następująca:

```csh
hostnamectl [opcje] [argumenty]
```

## Częste opcje
- `set-hostname`: Umożliwia ustawienie nowej nazwy hosta.
- `status`: Wyświetla aktualny status i informacje o systemie.
- `help`: Wyświetla pomoc dotyczącą użycia polecenia.

## Częste przykłady
1. **Wyświetlenie aktualnej nazwy hosta:**
   ```csh
   hostnamectl status
   ```

2. **Ustawienie nowej nazwy hosta:**
   ```csh
   hostnamectl set-hostname nowa-nazwa-host
   ```

3. **Wyświetlenie pomocy:**
   ```csh
   hostnamectl help
   ```

## Wskazówki
- Upewnij się, że masz odpowiednie uprawnienia (np. jako root), aby zmieniać nazwę hosta.
- Po zmianie nazwy hosta, rozważ ponowne uruchomienie systemu, aby upewnić się, że wszystkie usługi działają poprawnie z nową nazwą.
- Zawsze możesz użyć opcji `status`, aby sprawdzić, czy zmiany zostały zastosowane poprawnie.