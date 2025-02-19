# [Linux] C Shell (csh) curl użycie: Pobieranie danych z internetu

## Overview
Polecenie `curl` służy do przesyłania danych za pomocą różnych protokołów, takich jak HTTP, HTTPS, FTP i wielu innych. Umożliwia pobieranie plików, wysyłanie danych oraz interakcję z API.

## Usage
Podstawowa składnia polecenia `curl` wygląda następująco:

```csh
curl [opcje] [argumenty]
```

## Common Options
- `-O` - Pobiera plik i zapisuje go z oryginalną nazwą.
- `-o <nazwa_pliku>` - Pobiera plik i zapisuje go pod określoną nazwą.
- `-I` - Wysyła zapytanie HEAD i wyświetla nagłówki odpowiedzi.
- `-d <dane>` - Wysyła dane w żądaniu POST.
- `-H <nagłówek>` - Dodaje niestandardowy nagłówek do żądania.

## Common Examples
- Pobieranie pliku z internetu i zapisanie go z oryginalną nazwą:
  ```csh
  curl -O http://example.com/plik.txt
  ```

- Pobieranie pliku i zapisanie go pod inną nazwą:
  ```csh
  curl -o nowa_nazwa.txt http://example.com/plik.txt
  ```

- Wysyłanie zapytania HEAD i wyświetlanie nagłówków odpowiedzi:
  ```csh
  curl -I http://example.com
  ```

- Wysyłanie danych w żądaniu POST:
  ```csh
  curl -d "parametr1=wartosc1&parametr2=wartosc2" http://example.com/api
  ```

- Dodawanie niestandardowego nagłówka do żądania:
  ```csh
  curl -H "Authorization: Bearer token" http://example.com/api
  ```

## Tips
- Używaj opcji `-v`, aby uzyskać szczegółowe informacje o przesyłanych danych i odpowiedziach serwera.
- Sprawdzaj dokumentację `curl` za pomocą `man curl`, aby poznać wszystkie dostępne opcje.
- Zawsze testuj swoje zapytania w bezpiecznym środowisku przed użyciem ich w produkcji.