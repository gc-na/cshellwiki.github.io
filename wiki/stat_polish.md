# [Linux] C Shell (csh) stat <Użycie: wyświetlanie informacji o plikach>

## Przegląd
Polecenie `stat` w C Shell (csh) służy do wyświetlania szczegółowych informacji o plikach i katalogach, takich jak rozmiar, uprawnienia, czas modyfikacji i inne atrybuty.

## Użycie
Podstawowa składnia polecenia `stat` jest następująca:

```csh
stat [opcje] [argumenty]
```

## Typowe opcje
- `-c` : Umożliwia określenie formatu wyjścia.
- `-f` : Wyświetla informacje w formacie systemu plików.
- `-L` : Śledzi dowiązania symboliczne, wyświetlając informacje o pliku, do którego prowadzą.

## Przykłady
Oto kilka praktycznych przykładów użycia polecenia `stat`:

1. Wyświetlenie podstawowych informacji o pliku:
   ```csh
   stat plik.txt
   ```

2. Wyświetlenie informacji o katalogu:
   ```csh
   stat /ścieżka/do/katalogu
   ```

3. Użycie opcji `-c` do dostosowania formatu wyjścia:
   ```csh
   stat -c "Rozmiar: %s bajtów, Czas modyfikacji: %y" plik.txt
   ```

4. Śledzenie dowiązań symbolicznych:
   ```csh
   stat -L dowiazanie.txt
   ```

## Wskazówki
- Używaj opcji `-c`, aby dostosować wyjście do swoich potrzeb, co może być przydatne w skryptach.
- Sprawdzaj uprawnienia plików, aby upewnić się, że masz odpowiednie dostępy do plików, z którymi pracujesz.
- Regularnie korzystaj z `stat` w połączeniu z innymi poleceniami, aby uzyskać pełniejszy obraz stanu systemu plików.