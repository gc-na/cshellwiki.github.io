# [Linux] Bash dávkový příkaz: Spouštění příkazů v dávkách

## Přehled
Dávkový příkaz `batch` slouží k plánování a spouštění příkazů v pozadí, které se vykonají, když je systém méně vytížený. Umožňuje uživatelům zadávat příkazy, které se mají vykonat později, obvykle během doby nízkého zatížení systému.

## Použití
Základní syntaxe příkazu `batch` je následující:

```bash
batch [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Umožňuje specifikovat soubor, který obsahuje příkazy k vykonání.
- `-h`: Zobrazí nápovědu k příkazu.
- `-V`: Zobrazí verzi příkazu.

## Běžné příklady
1. **Zadání příkazů do dávky**:
   Chcete-li zadat příkazy, které se mají vykonat později, stačí spustit `batch` a poté zadat příkazy:
   ```bash
   batch
   at> echo "Hello, World!" > hello.txt
   at> exit
   ```

2. **Spuštění skriptu v dávce**:
   Pokud máte skript, který chcete spustit, můžete použít:
   ```bash
   batch < my_script.sh
   ```

3. **Použití s možností -f**:
   Pokud máte soubor s příkazy, můžete ho spustit pomocí:
   ```bash
   batch -f my_commands.txt
   ```

## Tipy
- Ujistěte se, že příkazy, které zadáváte, jsou správné, protože se vykonají bez dalšího potvrzení.
- Můžete použít příkaz `atq` k zobrazení naplánovaných úloh, které čekají na vykonání.
- Dbejte na to, aby systém nebyl příliš vytížený v době, kdy se dávkové úlohy spouští, aby se zajistila jejich efektivita.