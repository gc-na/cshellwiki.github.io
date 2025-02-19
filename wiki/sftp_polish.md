# [Linux] C Shell (csh) sftp użycie: przesyłanie plików przez SSH

## Overview
Polecenie `sftp` (Secure File Transfer Protocol) służy do bezpiecznego przesyłania plików między komputerami za pomocą protokołu SSH. Umożliwia zarówno przesyłanie plików w jedną stronę, jak i synchronizację katalogów.

## Usage
Podstawowa składnia polecenia `sftp` jest następująca:

```csh
sftp [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `sftp`:

- `-b <plik>`: Użyj pliku wsadowego do wykonania poleceń.
- `-C`: Włącz kompresję danych.
- `-o <opcja>`: Ustaw dodatkowe opcje SSH, np. `-oPort=2222`.
- `-P <port>`: Określ port, na którym działa serwer SFTP.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `sftp`:

1. Połączenie z serwerem SFTP:
   ```csh
   sftp user@hostname
   ```

2. Przesyłanie pliku z lokalnego systemu na serwer:
   ```csh
   put lokalny_plik.txt
   ```

3. Pobieranie pliku z serwera na lokalny system:
   ```csh
   get zdalny_plik.txt
   ```

4. Przesyłanie katalogu na serwer:
   ```csh
   put -r lokalny_katalog
   ```

5. Użycie pliku wsadowego do wykonania wielu poleceń:
   ```csh
   sftp -b polecenia.txt user@hostname
   ```

## Tips
- Zawsze używaj opcji `-C`, aby przyspieszyć transfer plików, zwłaszcza przy dużych plikach.
- Regularnie sprawdzaj dostępność serwera SFTP przed rozpoczęciem transferu.
- Używaj kluczy SSH do uwierzytelniania, aby zwiększyć bezpieczeństwo połączenia.