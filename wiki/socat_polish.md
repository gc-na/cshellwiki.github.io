# [Linux] C Shell (csh) socat użycie: Narzędzie do przekazywania danych między różnymi źródłami

## Overview
`socat` to potężne narzędzie do przekazywania danych, które umożliwia tworzenie połączeń między różnymi typami źródeł, takimi jak gniazda, pliki, terminale i inne. Może być używane do tunelowania, przekazywania portów oraz komunikacji między procesami.

## Usage
Podstawowa składnia polecenia `socat` jest następująca:

```bash
socat [opcje] [argumenty]
```

## Common Options
- `-d`: Włącza tryb debugowania, co pozwala na wyświetlanie dodatkowych informacji o działaniu polecenia.
- `-v`: Włącza tryb szczegółowy, który pokazuje przesyłane dane.
- `TCP:<adres>:<port>`: Umożliwia połączenie z zdalnym serwerem TCP.
- `UDP:<adres>:<port>`: Umożliwia połączenie z zdalnym serwerem UDP.
- `FILE:<ścieżka>`: Umożliwia odczyt lub zapis do pliku.

## Common Examples
Oto kilka praktycznych przykładów użycia `socat`:

1. **Przekazywanie portu TCP:**
   ```bash
   socat TCP-LISTEN:1234,fork TCP:localhost:5678
   ```
   To polecenie nasłuchuje na porcie 1234 i przekazuje połączenia do lokalnego portu 5678.

2. **Tunelowanie połączenia SSH:**
   ```bash
   socat TCP-LISTEN:2222,fork EXEC:"ssh user@remote_host"
   ```
   To polecenie tworzy lokalny port 2222, który przekazuje połączenia do zdalnego hosta przez SSH.

3. **Przekazywanie danych z pliku:**
   ```bash
   socat FILE:/path/to/file.txt STDOUT
   ```
   To polecenie odczytuje zawartość pliku `file.txt` i wyświetla ją na standardowym wyjściu.

4. **Przekazywanie danych między dwoma gniazdami:**
   ```bash
   socat TCP4-LISTEN:8080,fork TCP4:example.com:80
   ```
   To polecenie nasłuchuje na porcie 8080 i przekazuje dane do portu 80 na `example.com`.

## Tips
- Używaj opcji `-d` i `-v`, aby uzyskać więcej informacji o działaniu `socat`, co może pomóc w debugowaniu.
- Zawsze testuj swoje połączenia lokalnie przed wdrożeniem ich w środowisku produkcyjnym.
- Zwróć uwagę na prawa dostępu do plików, gdy używasz `socat` do odczytu lub zapisu danych.