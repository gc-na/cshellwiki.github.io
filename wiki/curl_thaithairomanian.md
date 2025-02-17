# [Română] Bash curl utilizare: Instrument pentru transferul de date

## Overview
Comanda `curl` este un instrument versatil utilizat pentru transferul de date prin intermediul protocolului URL. Aceasta permite utilizatorilor să efectueze cereri HTTP, FTP și multe altele, facilitând descărcarea sau încărcarea fișierelor și interacțiunea cu API-uri.

## Usage
Sintaxa de bază a comenzii `curl` este următoarea:

```bash
curl [options] [arguments]
```

## Common Options
- `-X`: Specifică metoda HTTP (de exemplu, GET, POST).
- `-d`: Trimite datele specificate în cererea POST.
- `-H`: Adaugă un header personalizat la cerere.
- `-o`: Salvează răspunsul într-un fișier local.
- `-I`: Obține doar header-urile răspunsului.

## Common Examples
1. **Descărcarea unui fișier**:
   ```bash
   curl -O https://example.com/file.txt
   ```

2. **Trimiterea unei cereri POST**:
   ```bash
   curl -X POST -d "param1=value1&param2=value2" https://example.com/api
   ```

3. **Adăugarea unui header personalizat**:
   ```bash
   curl -H "Authorization: Bearer token" https://example.com/protected
   ```

4. **Obținerea doar a header-urilor**:
   ```bash
   curl -I https://example.com
   ```

5. **Salvarea răspunsului într-un fișier**:
   ```bash
   curl -o response.txt https://example.com
   ```

## Tips
- Folosiți `-v` pentru a activa modul verbose, care oferă informații detaliate despre cererea și răspunsul HTTP.
- Testați cererile API cu `curl` înainte de a le implementa în cod pentru a verifica răspunsurile.
- Asigurați-vă că utilizați opțiunea `-L` pentru a urma redirecționările, dacă este necesar.