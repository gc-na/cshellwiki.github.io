# [Linux] Bash wall użycie: wysyłanie wiadomości do wszystkich użytkowników

## Overview
Polecenie `wall` (skrót od "write all") służy do wysyłania wiadomości do wszystkich zalogowanych użytkowników w systemie. Umożliwia administratorom i innym użytkownikom komunikację z innymi osobami korzystającymi z tego samego systemu.

## Usage
Podstawowa składnia polecenia `wall` jest następująca:

```bash
wall [opcje] [argumenty]
```

## Common Options
- `-n`: Nie wyświetlać nagłówka z informacjami o użytkowniku.
- `-s`: Wysyłać wiadomość w trybie cichym, bez wyświetlania znaku nowej linii na końcu.
- `-f`: Wczytać wiadomość z pliku.

## Common Examples

1. **Wysłanie prostego komunikatu:**

```bash
wall "Uwaga! System będzie wyłączony za 10 minut."
```

2. **Wysłanie komunikatu bez nagłówka:**

```bash
wall -n "Przerwa na lunch za 30 minut."
```

3. **Wysłanie wiadomości z pliku:**

```bash
wall -f /path/to/message.txt
```

4. **Wysłanie cichej wiadomości:**

```bash
wall -s "Zaraz rozpocznie się spotkanie."
```

## Tips
- Używaj `wall` w czasie, gdy wiesz, że użytkownicy są aktywni, aby zapewnić, że wiadomość dotrze do wszystkich.
- Staraj się być zwięzły i jasny w komunikatach, aby uniknąć nieporozumień.
- Możesz użyć `wall` w skryptach, aby automatycznie informować użytkowników o ważnych zdarzeniach w systemie.