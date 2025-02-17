# [Linux] Bash iostat Użycie: Monitorowanie wydajności systemu

## Overview
Polecenie `iostat` jest narzędziem do monitorowania wydajności systemu, które dostarcza informacji o użyciu procesora oraz statystykach wejścia/wyjścia dla urządzeń blokowych. Umożliwia to administratorom systemu analizowanie obciążenia i wydajności dysków oraz procesora.

## Usage
Podstawowa składnia polecenia `iostat` jest następująca:

```bash
iostat [opcje] [argumenty]
```

## Common Options
- `-c` – wyświetla tylko statystyki CPU.
- `-d` – wyświetla tylko statystyki urządzeń blokowych.
- `-x` – wyświetla rozszerzone statystyki dla urządzeń.
- `-m` – wyświetla wartości w megabajtach.
- `-t` – dodaje znacznik czasu do wyjścia.

## Common Examples
1. Wyświetlenie podstawowych statystyk CPU i urządzeń:
   ```bash
   iostat
   ```

2. Wyświetlenie tylko statystyk CPU:
   ```bash
   iostat -c
   ```

3. Wyświetlenie szczegółowych statystyk dla urządzeń blokowych:
   ```bash
   iostat -d -x
   ```

4. Wyświetlenie statystyk w megabajtach:
   ```bash
   iostat -m
   ```

5. Monitorowanie wydajności w regularnych odstępach czasu (np. co 5 sekund):
   ```bash
   iostat 5
   ```

## Tips
- Używaj opcji `-x`, aby uzyskać bardziej szczegółowe informacje o wydajności dysków, co może pomóc w identyfikacji problemów z wydajnością.
- Regularne monitorowanie systemu za pomocą `iostat` może pomóc w przewidywaniu potrzeb związanych z rozbudową sprzętu.
- Połącz `iostat` z innymi narzędziami, takimi jak `vmstat` lub `mpstat`, aby uzyskać pełniejszy obraz wydajności systemu.