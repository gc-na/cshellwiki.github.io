# [Linux] Bash curl použití: Získání dat z URL

## Přehled
Příkaz `curl` slouží k přenosu dat mezi serverem a klientem pomocí různých protokolů, jako je HTTP, HTTPS, FTP a další. Je široce používán pro stahování souborů, testování API a interakci s webovými službami.

## Použití
Základní syntaxe příkazu `curl` je následující:

```bash
curl [možnosti] [argumenty]
```

## Běžné možnosti
- `-O`: Uloží soubor s názvem, který je uveden v URL.
- `-L`: Sleduje přesměrování, pokud je URL přesměrována na jinou adresu.
- `-d`: Odesílá data jako POST požadavek.
- `-H`: Přidává hlavičky k požadavku.
- `-u`: Umožňuje autentizaci pomocí uživatelského jména a hesla.

## Běžné příklady
### Stahování souboru
Stáhněte soubor z URL a uložte ho s původním názvem:
```bash
curl -O https://example.com/soubor.txt
```

### Sledování přesměrování
Pokud je URL přesměrována, použijte tuto možnost:
```bash
curl -L https://example.com
```

### Odesílání dat pomocí POST
Odeslání dat na server jako POST požadavek:
```bash
curl -d "jmeno=Jan&prijmeni=Novak" -X POST https://example.com/api
```

### Přidání hlaviček
Přidání vlastních hlaviček k požadavku:
```bash
curl -H "Authorization: Bearer token" https://example.com/api
```

### Autentizace
Použití uživatelského jména a hesla pro přístup k chráněným zdrojům:
```bash
curl -u uzivatel:heslo https://example.com/chranene
```

## Tipy
- Vždy zkontrolujte, zda máte správně nastavené možnosti pro zabezpečení, zejména při práci s citlivými daty.
- Používejte `-v` pro podrobné výstupy, které vám pomohou při ladění problémů s připojením.
- Uložte často používané příkazy do skriptů pro snadnější opakované použití.