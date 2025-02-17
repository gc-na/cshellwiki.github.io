# [Linux] Bash netcat použití: Nástroj pro síťovou komunikaci

## Přehled
Netcat, často označovaný jako "švýcarský armádní nůž" pro síťovou komunikaci, je nástroj, který umožňuje číst a zapisovat data přes síťové spojení pomocí protokolů TCP nebo UDP. Je užitečný pro testování a diagnostiku síťových služeb.

## Použití
Základní syntaxe příkazu netcat je následující:

```bash
netcat [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Spustí netcat v režimu naslouchání.
- `-p`: Určuje port, na kterém má netcat naslouchat nebo se připojit.
- `-u`: Používá UDP místo TCP.
- `-v`: Aktivuje verbózní režim pro podrobnější výstup.
- `-z`: Provádí skenování portů bez odesílání dat.

## Běžné příklady
1. **Naslouchání na portu 1234:**
   ```bash
   netcat -l -p 1234
   ```

2. **Připojení k serveru na portu 80:**
   ```bash
   netcat example.com 80
   ```

3. **Odeslání souboru přes TCP:**
   ```bash
   netcat -l -p 1234 < soubor.txt
   ```

4. **Skenování portů na cílovém hostiteli:**
   ```bash
   netcat -z -v example.com 1-1000
   ```

5. **Přenos dat přes UDP:**
   ```bash
   netcat -u -l -p 1234
   ```

## Tipy
- Používejte `-v` pro získání více informací o tom, co se děje, zejména při ladění.
- Při skenování portů buďte opatrní, abyste se vyhnuli nechtěnému narušení služeb.
- Netcat může být použit jako jednoduchý server pro testování aplikací, což je užitečné při vývoji.