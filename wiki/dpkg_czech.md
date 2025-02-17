# [Linux] Bash dpkg použití: Správa balíčků v Debianu a jeho derivátech

## Přehled
Příkaz `dpkg` je základní nástroj pro správu balíčků v operačních systémech založených na Debianu, jako jsou Ubuntu a jejich deriváty. Umožňuje instalaci, odstranění a správu softwarových balíčků ve formátu `.deb`.

## Použití
Základní syntaxe příkazu `dpkg` je následující:

```bash
dpkg [možnosti] [argumenty]
```

## Běžné možnosti
- `-i`, `--install`: Nainstaluje balíček.
- `-r`, `--remove`: Odstraní nainstalovaný balíček.
- `-l`, `--list`: Zobrazí seznam nainstalovaných balíčků.
- `-s`, `--status`: Zobrazí informace o stavu balíčku.
- `-c`, `--contents`: Zobrazí obsah balíčku.

## Běžné příklady
1. **Instalace balíčku**:
   ```bash
   sudo dpkg -i balicek.deb
   ```

2. **Odstranění balíčku**:
   ```bash
   sudo dpkg -r nazev_balicku
   ```

3. **Zobrazení seznamu nainstalovaných balíčků**:
   ```bash
   dpkg -l
   ```

4. **Získání informací o balíčku**:
   ```bash
   dpkg -s nazev_balicku
   ```

5. **Zobrazení obsahu balíčku**:
   ```bash
   dpkg -c balicek.deb
   ```

## Tipy
- Při instalaci balíčků pomocí `dpkg` se ujistěte, že máte všechny potřebné závislosti. Pokud se vyskytnou problémy, můžete použít `apt-get install -f` k jejich automatickému vyřešení.
- Používejte `dpkg` v kombinaci s dalšími nástroji, jako je `apt`, pro efektivnější správu balíčků.
- Vždy zkontrolujte, zda je balíček, který chcete nainstalovat, důvěryhodný a pochází z ověřeného zdroje.