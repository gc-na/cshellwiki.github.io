# [Linux] Bash netcat użycie: Narzędzie do komunikacji sieciowej

## Overview
Netcat, znany również jako "nc", to wszechstronne narzędzie do komunikacji sieciowej, które umożliwia przesyłanie danych przez protokoły TCP i UDP. Jest często używane do testowania połączeń sieciowych, przesyłania plików oraz jako prosty serwer lub klient.

## Usage
Podstawowa składnia polecenia netcat wygląda następująco:

```bash
netcat [opcje] [argumenty]
```

## Common Options
- `-l` - Uruchamia netcat w trybie nasłuchu (serwer).
- `-p [port]` - Określa port, na którym netcat będzie nasłuchiwać lub łączyć się.
- `-u` - Używa protokołu UDP zamiast TCP.
- `-v` - Włącza tryb szczegółowy, wyświetlając dodatkowe informacje o połączeniu.
- `-w [czas]` - Ustala czas oczekiwania na połączenie.

## Common Examples
### Prosty serwer TCP
Aby uruchomić prosty serwer TCP nasłuchujący na porcie 1234:

```bash
netcat -l -p 1234
```

### Klient TCP łączący się z serwerem
Aby połączyć się z serwerem TCP działającym na adresie IP 192.168.1.1 i porcie 1234:

```bash
netcat 192.168.1.1 1234
```

### Przesyłanie pliku
Aby przesłać plik `example.txt` z jednego komputera do drugiego:

Na komputerze odbierającym:

```bash
netcat -l -p 1234 > example.txt
```

Na komputerze wysyłającym:

```bash
netcat 192.168.1.2 1234 < example.txt
```

### Użycie protokołu UDP
Aby wysłać wiadomość za pomocą protokołu UDP:

```bash
echo "Wiadomość UDP" | netcat -u 192.168.1.2 1234
```

## Tips
- Używaj opcji `-v`, aby uzyskać więcej informacji o połączeniach, co może pomóc w debugowaniu.
- Pamiętaj, aby sprawdzić, czy porty są otwarte w zaporze sieciowej, aby umożliwić połączenia.
- Netcat może być używany do testowania zabezpieczeń, ale należy zachować ostrożność i używać go tylko w dozwolonych środowiskach.