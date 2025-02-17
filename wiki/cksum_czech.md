# [Linux] Bash cksum použití: Vypočítá kontrolní součet souboru

## Přehled
Příkaz `cksum` slouží k výpočtu kontrolního součtu a velikosti souboru. Vytváří jedinečný identifikátor pro obsah souboru, což je užitečné pro ověřování integrity dat.

## Použití
Základní syntaxe příkazu je následující:

```bash
cksum [možnosti] [argumenty]
```

## Běžné možnosti
- `-a, --algorithm=ALG` - Určuje algoritmus pro výpočet kontrolního součtu (např. md5, sha256).
- `--help` - Zobrazí nápovědu k příkazu.
- `--version` - Zobrazí verzi příkazu.

## Běžné příklady
1. **Základní použití pro výpočet kontrolního součtu souboru:**

   ```bash
   cksum soubor.txt
   ```

2. **Výpočet kontrolního součtu pro více souborů:**

   ```bash
   cksum soubor1.txt soubor2.txt
   ```

3. **Použití s volbou pro zobrazení nápovědy:**

   ```bash
   cksum --help
   ```

4. **Výpočet kontrolního součtu s určením algoritmu:**

   ```bash
   cksum --algorithm=md5 soubor.txt
   ```

## Tipy
- Používejte `cksum` při přenosu souborů pro ověření, že se obsah nezměnil.
- Uložte výstup příkazu do souboru pro pozdější porovnání.
- Kombinujte `cksum` s dalšími příkazy, jako je `grep`, pro filtrování výsledků.