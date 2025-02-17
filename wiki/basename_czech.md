# [Linux] Bash basename použití: Získání názvu souboru bez cesty

## Přehled
Příkaz `basename` se používá k extrakci názvu souboru z úplné cesty. Odstraní všechny předchozí adresáře a vrátí pouze poslední část cesty, což je název souboru nebo adresáře.

## Použití
Základní syntaxe příkazu je následující:

```bash
basename [options] [arguments]
```

## Běžné možnosti
- `-a`: Zpracovává více argumentů a vrací názvy souborů pro každý z nich.
- `-s`: Odstraní zadanou příponu z názvu souboru.
- `--help`: Zobrazí nápovědu k příkazu.

## Běžné příklady
1. Získání názvu souboru z cesty:
   ```bash
   basename /home/uzivatel/dokumenty/soubor.txt
   ```
   Výstup: `soubor.txt`

2. Získání názvu adresáře:
   ```bash
   basename /var/log/syslog
   ```
   Výstup: `syslog`

3. Odstranění přípony z názvu souboru:
   ```bash
   basename /home/uzivatel/dokumenty/soubor.txt .txt
   ```
   Výstup: `soubor`

4. Zpracování více souborů najednou:
   ```bash
   basename -a /home/uzivatel/dokumenty/soubor1.txt /home/uzivatel/dokumenty/soubor2.txt
   ```
   Výstup:
   ```
   soubor1.txt
   soubor2.txt
   ```

## Tipy
- Pokud potřebujete získat pouze název souboru bez přípony, můžete použít kombinaci `basename` a `cut` pro větší flexibilitu.
- Při práci s více soubory je užitečné použít možnost `-a`, abyste se vyhnuli opakování příkazu pro každý soubor zvlášť.
- Ujistěte se, že cesty k souborům jsou správné, aby příkaz fungoval bez chyb.