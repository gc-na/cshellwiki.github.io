# [Linux] Bash rsync použití: Synchronizace souborů a adresářů

## Přehled
Rsync je mocný nástroj pro synchronizaci souborů a adresářů mezi různými místy. Umožňuje efektivní přenos dat, protože přenáší pouze změněné části souborů, což šetří čas a šířku pásma.

## Použití
Základní syntaxe příkazu rsync je následující:

```bash
rsync [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Archivní režim, který zahrnuje rekurzivní kopírování a zachování atributů souborů.
- `-v`: Verbózní výstup, který zobrazuje podrobnosti o procesu.
- `-z`: Komprese dat během přenosu, což zrychluje přenos velkých souborů.
- `-r`: Rekurzivní kopírování adresářů.
- `--delete`: Odstraní soubory v cílovém umístění, které nejsou v zdrojovém umístění.

## Běžné příklady
1. **Základní synchronizace souborů:**
   ```bash
   rsync -av /cesta/k/zdroji/ /cesta/k/cíli/
   ```

2. **Synchronizace s kompresí:**
   ```bash
   rsync -avz /cesta/k/zdroji/ /cesta/k/cíli/
   ```

3. **Synchronizace a odstranění neexistujících souborů v cíli:**
   ```bash
   rsync -av --delete /cesta/k/zdroji/ /cesta/k/cíli/
   ```

4. **Synchronizace přes SSH:**
   ```bash
   rsync -avz -e ssh /cesta/k/zdroji/ uživatel@server:/cesta/k/cíli/
   ```

## Tipy
- Před provedením příkazu s možností `--delete` doporučujeme provést testovací synchronizaci s možností `-n` (suchý běh), abyste viděli, co bude smazáno.
- Používejte `-v` pro sledování pokroku a diagnostiku případných problémů.
- Pokud synchronizujete velké množství dat, zvažte použití `--progress`, abyste viděli průběh přenosu.