# [Linux] Bash curl użycie: Pobieranie i wysyłanie danych przez URL

## Overview
Polecenie `curl` jest narzędziem wiersza poleceń, które umożliwia przesyłanie danych do lub z serwera przy użyciu różnych protokołów, w tym HTTP, HTTPS, FTP i wielu innych. Jest często używane do pobierania plików, testowania API oraz interakcji z serwisami internetowymi.

## Usage
Podstawowa składnia polecenia `curl` jest następująca:

```bash
curl [opcje] [argumenty]
```

## Common Options
Oto kilka powszechnie używanych opcji dla `curl`:

- `-O` - Pobiera plik i zapisuje go z oryginalną nazwą.
- `-o [plik]` - Pobiera plik i zapisuje go pod określoną nazwą.
- `-I` - Wysyła zapytanie HEAD i wyświetla nagłówki odpowiedzi.
- `-d [dane]` - Wysyła dane w ciele żądania (przydatne w przypadku POST).
- `-H [nagłówek]` - Dodaje nagłówek do żądania.
- `-u [użytkownik:hasło]` - Używa podanych danych do autoryzacji.

## Common Examples
Oto kilka praktycznych przykładów użycia `curl`:

1. **Pobieranie pliku z internetu:**

   ```bash
   curl -O https://example.com/plik.txt
   ```

2. **Pobieranie pliku i zapisanie go pod inną nazwą:**

   ```bash
   curl -o nowa_nazwa.txt https://example.com/plik.txt
   ```

3. **Wysyłanie zapytania GET do API:**

   ```bash
   curl https://api.example.com/dane
   ```

4. **Wysyłanie danych za pomocą metody POST:**

   ```bash
   curl -d "nazwa=Jan&wiek=30" -X POST https://api.example.com/użytkownik
   ```

5. **Dodawanie nagłówka do zapytania:**

   ```bash
   curl -H "Authorization: Bearer token" https://api.example.com/chronione-dane
   ```

## Tips
- Używaj opcji `-I`, aby szybko sprawdzić nagłówki odpowiedzi bez pobierania całej zawartości.
- Zawsze sprawdzaj dokumentację API, aby wiedzieć, jakie nagłówki i dane są wymagane.
- Możesz używać `curl` w skryptach Bash, aby automatyzować interakcje z serwisami internetowymi.