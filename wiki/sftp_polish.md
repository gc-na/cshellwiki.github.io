# [Linux] Bash sftp użycie: Przesyłanie plików przez SSH

## Overview
Polecenie `sftp` (Secure File Transfer Protocol) służy do bezpiecznego przesyłania plików pomiędzy komputerami za pomocą protokołu SSH. Umożliwia zarówno przesyłanie, jak i pobieranie plików w sposób zaszyfrowany, co zapewnia bezpieczeństwo danych.

## Usage
Podstawowa składnia polecenia `sftp` wygląda następująco:

```bash
sftp [opcje] [użytkownik@host]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `sftp`:

- `-P <port>`: Określa port, na którym nasłuchuje serwer SFTP.
- `-o <opcje>`: Umożliwia przekazanie dodatkowych opcji do klienta SSH.
- `-r`: Umożliwia rekurencyjne przesyłanie katalogów.

## Common Examples
Poniżej znajdują się przykłady użycia polecenia `sftp`:

### Połączenie z serwerem SFTP
Aby połączyć się z serwerem SFTP:

```bash
sftp użytkownik@host
```

### Przesyłanie pliku na serwer
Aby przesłać plik na serwer SFTP:

```bash
put lokalny_plik.txt
```

### Pobieranie pliku z serwera
Aby pobrać plik z serwera SFTP:

```bash
get zdalny_plik.txt
```

### Przesyłanie katalogu
Aby przesłać cały katalog na serwer SFTP:

```bash
put -r lokalny_katalog
```

### Zmiana katalogu na serwerze
Aby przejść do innego katalogu na serwerze SFTP:

```bash
cd zdalny_katalog
```

## Tips
- Używaj opcji `-P`, jeśli serwer SFTP działa na niestandardowym porcie.
- Zawsze sprawdzaj, czy połączenie jest bezpieczne, zwracając uwagę na komunikaty o kluczu hosta.
- Regularnie aktualizuj swoje oprogramowanie SSH, aby zapewnić sobie najnowsze poprawki bezpieczeństwa.