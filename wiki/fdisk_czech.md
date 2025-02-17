# [Linux] Bash fdisk použití: Správa diskových oddílů

## Přehled
Příkaz `fdisk` slouží k vytváření, mazání a správě diskových oddílů na pevných discích a dalších úložných zařízeních. Umožňuje uživatelům manipulovat s tabulkami oddílů a provádět různé operace související s diskovým úložištěm.

## Použití
Základní syntaxe příkazu `fdisk` je následující:

```bash
fdisk [možnosti] [argumenty]
```

## Běžné možnosti
- `-l`: Vypíše seznam všech dostupných diskových oddílů.
- `-u`: Používá jednotky v sektorech místo bloků.
- `-n`: Vytvoří nový oddíl.
- `-d`: Smaže existující oddíl.
- `-p`: Vytiskne aktuální tabulku oddílů.

## Běžné příklady
1. **Zobrazit seznam diskových oddílů:**
   ```bash
   fdisk -l
   ```

2. **Otevřít konkrétní disk pro úpravy (např. /dev/sda):**
   ```bash
   fdisk /dev/sda
   ```

3. **Vytvořit nový oddíl:**
   Po spuštění `fdisk /dev/sda`, použijte příkaz `n` a postupujte podle pokynů.

4. **Smazat oddíl:**
   Po spuštění `fdisk /dev/sda`, použijte příkaz `d` a zadejte číslo oddílu, který chcete smazat.

5. **Vytisknout aktuální tabulku oddílů:**
   Po spuštění `fdisk /dev/sda`, použijte příkaz `p`.

## Tipy
- Před prováděním změn na oddílech vždy zálohujte důležitá data.
- Používejte příkaz `fdisk` s opatrností, protože nesprávné operace mohou vést ke ztrátě dat.
- Po provedení změn nezapomeňte použít příkaz `w` pro uložení změn a ukončení `fdisk`.