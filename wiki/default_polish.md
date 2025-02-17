# [Linux] Bash domyślny polecenie: [wyświetlanie zawartości plików]

## Przegląd
Polecenie `cat` w systemie Linux służy do wyświetlania zawartości plików tekstowych. Może być również używane do łączenia kilku plików w jeden oraz do tworzenia nowych plików.

## Użycie
Podstawowa składnia polecenia `cat` wygląda następująco:

```bash
cat [opcje] [argumenty]
```

## Często używane opcje
- `-n`: Numeruje wszystkie linie w wyjściu.
- `-b`: Numeruje tylko niepuste linie.
- `-E`: Wyświetla znak końca linii `$` na końcu każdej linii.
- `-s`: Usuwa puste linie.

## Przykłady
1. Wyświetlenie zawartości pliku:
   ```bash
   cat plik.txt
   ```

2. Wyświetlenie zawartości kilku plików:
   ```bash
   cat plik1.txt plik2.txt
   ```

3. Połączenie kilku plików w jeden:
   ```bash
   cat plik1.txt plik2.txt > nowy_plik.txt
   ```

4. Wyświetlenie zawartości pliku z numerami linii:
   ```bash
   cat -n plik.txt
   ```

5. Usunięcie pustych linii z wyjścia:
   ```bash
   cat -s plik.txt
   ```

## Wskazówki
- Używaj opcji `-n` lub `-b`, aby lepiej zrozumieć strukturę pliku, zwłaszcza w dłuższych dokumentach.
- Możesz użyć `cat` w połączeniu z innymi poleceniami, na przykład `grep`, aby przeszukiwać zawartość plików.
- Pamiętaj, że `cat` jest najlepsze do pracy z plikami tekstowymi; nie używaj go do wyświetlania plików binarnych, ponieważ może to prowadzić do nieczytelnych danych.