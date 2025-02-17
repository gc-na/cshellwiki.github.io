# [Linux] Bash pidstat użycie: Monitorowanie statystyk procesów

## Overview
Polecenie `pidstat` jest narzędziem do monitorowania statystyk procesów w systemie Linux. Umożliwia użytkownikom śledzenie wykorzystania CPU, pamięci oraz innych zasobów przez konkretne procesy, co jest przydatne w diagnostyce i optymalizacji wydajności systemu.

## Usage
Podstawowa składnia polecenia `pidstat` wygląda następująco:

```bash
pidstat [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `pidstat`:

- `-h`: Wyświetla nagłówki w formacie bardziej czytelnym.
- `-r`: Pokazuje statystyki użycia pamięci.
- `-u`: Wyświetla statystyki CPU.
- `-p <pid>`: Monitoruje konkretne procesy na podstawie ich identyfikatora PID.
- `-t`: Pokazuje statystyki dla wszystkich wątków w procesie.

## Common Examples

1. **Monitorowanie użycia CPU dla wszystkich procesów:**
   ```bash
   pidstat -u
   ```

2. **Monitorowanie użycia pamięci dla wszystkich procesów:**
   ```bash
   pidstat -r
   ```

3. **Monitorowanie konkretnego procesu o PID 1234:**
   ```bash
   pidstat -p 1234
   ```

4. **Wyświetlanie statystyk dla wszystkich wątków w procesie o PID 5678:**
   ```bash
   pidstat -t -p 5678
   ```

5. **Monitorowanie statystyk co 2 sekundy:**
   ```bash
   pidstat 2
   ```

## Tips
- Używaj opcji `-h`, aby uzyskać bardziej czytelne nagłówki, co ułatwia analizę wyników.
- Regularne monitorowanie procesów może pomóc w identyfikacji problemów z wydajnością, dlatego warto zautomatyzować to zadanie przy użyciu skryptów.
- Możesz łączyć `pidstat` z innymi narzędziami, takimi jak `grep`, aby filtrować wyniki i skupić się na interesujących cię procesach.