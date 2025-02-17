# [Linux] Bash setopt použití: Nastavení chování shellu

## Přehled
Příkaz `setopt` se používá v shellu Zsh k aktivaci nebo deaktivaci různých možností, které ovlivňují chování shellu. Umožňuje uživatelům přizpůsobit prostředí podle svých potřeb a preferencí.

## Použití
Základní syntaxe příkazu `setopt` je následující:

```bash
setopt [možnosti] [argumenty]
```

## Běžné možnosti
- `noclobber`: Zabraňuje přepsání existujících souborů při přesměrování výstupu.
- `noexec`: Zabraňuje provádění skriptů, což je užitečné pro testování.
- `allexport`: Automaticky exportuje všechny proměnné do prostředí podřízených procesů.
- `ignoreeof`: Zabraňuje ukončení shellu pomocí Ctrl+D.

## Běžné příklady
1. Aktivace možnosti `noclobber`:
   ```bash
   setopt noclobber
   ```

2. Deaktivace možnosti `noexec`:
   ```bash
   setopt noexec
   ```

3. Aktivace možnosti `allexport`:
   ```bash
   setopt allexport
   ```

4. Aktivace možnosti `ignoreeof`:
   ```bash
   setopt ignoreeof
   ```

## Tipy
- Před aktivací možnosti `noclobber` se ujistěte, že máte zálohy důležitých souborů, abyste se vyhnuli ztrátě dat.
- Používejte `setopt` v souboru `.zshrc`, abyste trvale nastavili preferované možnosti při každém spuštění shellu.
- Zkontrolujte aktuální nastavení pomocí příkazu `set`, který zobrazí všechny aktivní možnosti.