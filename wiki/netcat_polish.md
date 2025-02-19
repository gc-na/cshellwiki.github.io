# [Linux] C Shell (csh) netcat użycie: Narzędzie do komunikacji sieciowej

## Przegląd
Netcat, znany również jako "nc", to wszechstronne narzędzie do komunikacji sieciowej, które umożliwia przesyłanie danych między komputerami przez protokoły TCP i UDP. Jest często używane do debugowania i testowania połączeń sieciowych oraz do przesyłania plików.

## Użycie
Podstawowa składnia polecenia netcat wygląda następująco:

```
netcat [opcje] [argumenty]
```

## Częste opcje
- `-l` - nasłuchuj na porcie (tryb serwera).
- `-p [port]` - określ port do użycia.
- `-u` - użyj protokołu UDP zamiast TCP.
- `-v` - włącz tryb szczegółowy (verbose).
- `-w [czas]` - ustaw czas oczekiwania na połączenie.

## Częste przykłady
1. **Nasłuchiwanie na porcie 1234:**
   ```bash
   netcat -l -p 1234
   ```

2. **Wysyłanie wiadomości do serwera na porcie 1234:**
   ```bash
   echo "Witaj, świecie!" | netcat localhost 1234
   ```

3. **Przesyłanie pliku:**
   Na serwerze:
   ```bash
   netcat -l -p 1234 > plik.txt
   ```
   Na kliencie:
   ```bash
   netcat localhost 1234 < plik.txt
   ```

4. **Testowanie połączenia TCP:**
   ```bash
   netcat -v example.com 80
   ```

5. **Nasłuchiwanie na porcie UDP:**
   ```bash
   netcat -u -l -p 1234
   ```

## Wskazówki
- Używaj opcji `-v`, aby uzyskać więcej informacji o połączeniach i błędach.
- Zawsze upewnij się, że porty, których używasz, są otwarte i dostępne w zaporze sieciowej.
- Netcat może być używany do testowania bezpieczeństwa, ale pamiętaj o etyce i przepisach prawnych dotyczących testowania systemów.