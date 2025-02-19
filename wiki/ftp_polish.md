# [Linux] C Shell (csh) ftp użycie: Przesyłanie plików przez protokół FTP

## Overview
Polecenie `ftp` w C Shell (csh) służy do przesyłania plików między komputerem a serwerem FTP. Umożliwia użytkownikom łączenie się z serwerami, pobieranie plików oraz przesyłanie ich na serwer.

## Usage
Podstawowa składnia polecenia `ftp` wygląda następująco:

```
ftp [opcje] [argumenty]
```

## Common Options
- `-v`: Włącza tryb szczegółowy, wyświetlając więcej informacji o połączeniu.
- `-n`: Nie nawiązuje automatycznie połączenia z serwerem przy starcie.
- `-i`: Wyłącza tryb interaktywny, co pozwala na przesyłanie plików bez potwierdzenia.
- `-g`: Wyłącza globbing, co pozwala na przesyłanie plików z nazwami zawierającymi znaki specjalne.

## Common Examples
### Połączenie z serwerem FTP
Aby połączyć się z serwerem FTP, użyj polecenia:

```
ftp ftp.example.com
```

### Pobieranie pliku
Aby pobrać plik z serwera, użyj polecenia `get`:

```
get nazwa_pliku.txt
```

### Przesyłanie pliku
Aby przesłać plik na serwer, użyj polecenia `put`:

```
put lokalny_plik.txt
```

### Zmiana katalogu
Aby zmienić katalog na serwerze FTP, użyj polecenia `cd`:

```
cd katalog_na_serwerze
```

### Wyświetlanie zawartości katalogu
Aby wyświetlić zawartość katalogu na serwerze, użyj polecenia `ls`:

```
ls
```

## Tips
- Zawsze sprawdzaj, czy masz odpowiednie uprawnienia do przesyłania lub pobierania plików.
- Używaj opcji `-v`, aby uzyskać więcej informacji o procesie transferu.
- Pamiętaj o wylogowaniu się z serwera FTP po zakończeniu pracy, używając polecenia `bye`.