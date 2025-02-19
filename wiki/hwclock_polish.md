# [Linux] C Shell (csh) hwclock użycie: zarządzanie zegarem sprzętowym

## Overview
Polecenie `hwclock` służy do odczytywania i ustawiania czasu zegara sprzętowego w systemie. Zegar sprzętowy, znany również jako zegar BIOS, działa niezależnie od systemu operacyjnego i jest używany do przechowywania czasu, nawet gdy komputer jest wyłączony.

## Usage
Podstawowa składnia polecenia `hwclock` jest następująca:

```
hwclock [opcje] [argumenty]
```

## Common Options
- `--show` - Wyświetla aktualny czas zegara sprzętowego.
- `--set` - Ustawia czas zegara sprzętowego na podany czas.
- `--hctosys` - Ustawia czas systemowy na czas zegara sprzętowego.
- `--systohc` - Ustawia czas zegara sprzętowego na czas systemowy.
- `--utc` - Używa czasu UTC (Coordinated Universal Time).

## Common Examples
1. Wyświetlenie aktualnego czasu zegara sprzętowego:
   ```bash
   hwclock --show
   ```

2. Ustawienie zegara sprzętowego na określoną datę i godzinę:
   ```bash
   hwclock --set --date="2023-10-01 12:00:00"
   ```

3. Ustawienie czasu systemowego na czas zegara sprzętowego:
   ```bash
   hwclock --hctosys
   ```

4. Ustawienie zegara sprzętowego na czas systemowy:
   ```bash
   hwclock --systohc
   ```

5. Wyświetlenie czasu zegara sprzętowego w formacie UTC:
   ```bash
   hwclock --show --utc
   ```

## Tips
- Upewnij się, że masz odpowiednie uprawnienia (zazwyczaj wymagane są uprawnienia administratora) do zmiany ustawień zegara sprzętowego.
- Regularnie synchronizuj czas systemowy z zegarem sprzętowym, aby uniknąć rozbieżności.
- W przypadku korzystania z systemów wielozadaniowych, rozważ użycie `ntp` do automatycznej synchronizacji czasu.