# [Linux] Bash ulimit použití: Ovládání systémových limitů

## Přehled
Příkaz `ulimit` slouží k nastavení nebo zobrazení systémových limitů pro procesy běžící v shellu. Tyto limity mohou zahrnovat maximální velikost souborů, maximální počet otevřených souborů a další zdroje, které mohou ovlivnit výkon a stabilitu systému.

## Použití
Základní syntaxe příkazu `ulimit` je následující:

```bash
ulimit [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Zobrazí všechny aktuální limity.
- `-c`: Nastaví maximální velikost core souboru.
- `-d`: Nastaví maximální velikost datového segmentu.
- `-f`: Nastaví maximální velikost souboru, který může být vytvořen.
- `-n`: Nastaví maximální počet otevřených souborů.
- `-s`: Nastaví maximální velikost zásobníku.
- `-t`: Nastaví maximální čas CPU pro proces.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ulimit`:

1. Zobrazení všech aktuálních limitů:
   ```bash
   ulimit -a
   ```

2. Nastavení maximální velikosti souboru na 100 MB:
   ```bash
   ulimit -f 102400
   ```

3. Nastavení maximálního počtu otevřených souborů na 2048:
   ```bash
   ulimit -n 2048
   ```

4. Zobrazení maximální velikosti zásobníku:
   ```bash
   ulimit -s
   ```

5. Nastavení maximální velikosti core souboru na 0 (zakázání core dump):
   ```bash
   ulimit -c 0
   ```

## Tipy
- Při nastavování limitů buďte opatrní, protože příliš nízké hodnoty mohou způsobit selhání aplikací.
- Uložení změn do souboru `~/.bashrc` nebo `~/.bash_profile` zajistí, že se limity použijí při každém spuštění shellu.
- Používejte `ulimit -a` k rychlému zobrazení všech aktuálních limitů a jejich hodnot.