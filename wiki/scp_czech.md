# [Linux] Bash scp použití: Přenos souborů mezi servery

## Přehled
Příkaz `scp` (Secure Copy Protocol) slouží k bezpečnému přenosu souborů mezi různými počítači přes síť. Využívá protokol SSH pro šifrování dat, což zajišťuje bezpečnost přenášených informací.

## Použití
Základní syntaxe příkazu `scp` je následující:

```bash
scp [možnosti] [zdroj] [cílová adresa]
```

## Běžné možnosti
- `-r`: Přenést adresář rekurzivně.
- `-P`: Určit port pro SSH (pokud není standardní 22).
- `-i`: Použít specifický soubor s privátním klíčem pro autentizaci.
- `-v`: Aktivovat podrobné výstupy pro ladění.

## Běžné příklady
1. **Přenos souboru z místního počítače na vzdálený server:**
   ```bash
   scp /cesta/k/souboru.txt uživatel@server:/cesta/k/cíli/
   ```

2. **Přenos souboru ze vzdáleného serveru na místní počítač:**
   ```bash
   scp uživatel@server:/cesta/k/souboru.txt /cesta/k/cíli/
   ```

3. **Přenos celého adresáře na vzdálený server:**
   ```bash
   scp -r /cesta/k/adresáři uživatel@server:/cesta/k/cíli/
   ```

4. **Přenos souboru na specifickém portu:**
   ```bash
   scp -P 2222 /cesta/k/souboru.txt uživatel@server:/cesta/k/cíli/
   ```

## Tipy
- Při přenosu citlivých dat vždy používejte `scp`, abyste zajistili šifrování.
- Pokud často přenášíte soubory mezi stejnými servery, zvažte nastavení SSH klíčů pro usnadnění autentizace.
- Používejte volbu `-v` pro diagnostiku problémů, pokud se přenos nezdaří.