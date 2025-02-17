# [Linux] Bash history użycie: przeglądanie historii poleceń

## Overview
Polecenie `history` w Bashu służy do wyświetlania listy wcześniej wykonanych poleceń. Umożliwia użytkownikom przeglądanie i ponowne używanie wcześniejszych komend, co znacznie przyspiesza pracę w terminalu.

## Usage
Podstawowa składnia polecenia `history` wygląda następująco:

```bash
history [options] [arguments]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `history`:

- `-c` - Czyści historię poleceń.
- `-d <n>` - Usuwa polecenie o numerze `n` z historii.
- `-a` - Zapisuje bieżącą historię do pliku historii.
- `-r` - Odczytuje historię z pliku historii.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `history`:

1. **Wyświetlenie całej historii poleceń:**
   ```bash
   history
   ```

2. **Wyświetlenie ostatnich 10 poleceń:**
   ```bash
   history 10
   ```

3. **Usunięcie konkretnego polecenia z historii (np. polecenie o numerze 5):**
   ```bash
   history -d 5
   ```

4. **Czyszczenie całej historii poleceń:**
   ```bash
   history -c
   ```

5. **Zapisanie bieżącej historii do pliku:**
   ```bash
   history -a
   ```

## Tips
- Użyj `!n`, aby szybko wykonać polecenie o numerze `n` z historii.
- Możesz przeszukiwać historię, używając kombinacji klawiszy `Ctrl + r`, aby znaleźć wcześniejsze polecenia.
- Regularnie czyść historię, aby uniknąć przechowywania niepotrzebnych lub wrażliwych informacji.