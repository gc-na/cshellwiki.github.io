# [Linux] C Shell (csh) diff <Porównywanie plików>: Porównuje różnice między plikami

## Overview
Polecenie `diff` w C Shell (csh) służy do porównywania dwóch plików tekstowych i wyświetlania różnic między nimi. Jest to przydatne narzędzie dla programistów i osób pracujących z tekstem, które chcą zobaczyć, co się zmieniło w plikach.

## Usage
Podstawowa składnia polecenia `diff` jest następująca:

```csh
diff [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `diff`:

- `-u`: Wyświetla różnice w formacie z kontekstem (unified).
- `-c`: Wyświetla różnice w formacie kontekstowym.
- `-i`: Ignoruje różnice w wielkości liter.
- `-w`: Ignoruje różnice w białych znakach.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `diff`:

1. Porównanie dwóch plików tekstowych:
   ```csh
   diff plik1.txt plik2.txt
   ```

2. Porównanie z ignorowaniem wielkości liter:
   ```csh
   diff -i plik1.txt plik2.txt
   ```

3. Wyświetlenie różnic w formacie z kontekstem:
   ```csh
   diff -u plik1.txt plik2.txt
   ```

4. Porównanie dwóch katalogów:
   ```csh
   diff -r katalog1/ katalog2/
   ```

## Tips
- Używaj opcji `-u`, aby uzyskać bardziej czytelny wynik, szczególnie przy większych zmianach.
- Przechowuj kopie zapasowe plików przed ich modyfikacją, aby móc łatwo porównać zmiany.
- Jeśli często porównujesz te same pliki, rozważ użycie skryptu, aby zautomatyzować proces.