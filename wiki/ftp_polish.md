# [Linux] Bash ftp użycie: Protokół transferu plików

## Overview
Polecenie `ftp` (File Transfer Protocol) służy do przesyłania plików między komputerami w sieci. Umożliwia nawiązywanie połączeń z serwerami FTP, co pozwala na pobieranie i wysyłanie plików.

## Usage
Podstawowa składnia polecenia `ftp` wygląda następująco:

```bash
ftp [opcje] [adres_serwera]
```

## Common Options
Oto kilka powszechnie używanych opcji dla polecenia `ftp`:

- `-i`: Wyłącza tryb interaktywny, co pozwala na przesyłanie plików bez potwierdzenia.
- `-n`: Nie nawiązuje automatycznie połączenia z serwerem po uruchomieniu.
- `-v`: Włącza tryb szczegółowy, wyświetlając więcej informacji o połączeniu.
- `-g`: Wyłącza globbing, co pozwala na przesyłanie plików z nazwami zawierającymi znaki specjalne.

## Common Examples
Oto kilka praktycznych przykładów użycia polecenia `ftp`:

1. **Nawiązanie połączenia z serwerem FTP:**
   ```bash
   ftp ftp.example.com
   ```

2. **Nawiązanie połączenia bez automatycznego logowania:**
   ```bash
   ftp -n ftp.example.com
   ```

3. **Pobranie pliku z serwera:**
   ```bash
   get nazwa_pliku.txt
   ```

4. **Wysłanie pliku na serwer:**
   ```bash
   put lokalny_plik.txt
   ```

5. **Pobranie wszystkich plików z katalogu:**
   ```bash
   mget *
   ```

## Tips
- Używaj opcji `-i`, gdy przesyłasz wiele plików, aby uniknąć potwierdzeń dla każdego z nich.
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do przesyłania lub pobierania plików z serwera.
- Jeśli często łączysz się z tym samym serwerem, rozważ utworzenie skryptu, aby uprościć proces logowania i przesyłania plików.