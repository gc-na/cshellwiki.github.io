# [Linux] Bash tee použití: Zapisování výstupu do souboru a na obrazovku

## Přehled
Příkaz `tee` se používá k čtení standardního vstupu a zapisování jeho obsahu jak do standardního výstupu (obvykle na obrazovku), tak do jednoho nebo více souborů. Tento příkaz je užitečný, když chcete sledovat výstup příkazu a zároveň ho uložit pro pozdější použití.

## Použití
Základní syntaxe příkazu `tee` je následující:

```bash
tee [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`, `--append`: Přidá výstup na konec souboru místo jeho přepsání.
- `-i`, `--ignore-interrupts`: Ignoruje přerušení (např. Ctrl+C).
- `--help`: Zobrazí nápovědu k příkazu.
- `--version`: Zobrazí verzi příkazu.

## Běžné příklady
1. **Zapisování výstupu příkazu do souboru:**

```bash
echo "Hello, world!" | tee output.txt
```

Tento příkaz zapíše text "Hello, world!" do souboru `output.txt` a zároveň ho zobrazí na obrazovce.

2. **Přidání výstupu do existujícího souboru:**

```bash
echo "Další řádek" | tee -a output.txt
```

Tento příkaz přidá text "Další řádek" na konec souboru `output.txt`.

3. **Zapisování výstupu více příkazů do souboru:**

```bash
ls -l | tee output.txt
```

Tento příkaz zapíše výstup příkazu `ls -l` do souboru `output.txt` a zároveň ho zobrazí na obrazovce.

4. **Zapisování výstupu do více souborů:**

```bash
echo "Zpráva" | tee soubor1.txt soubor2.txt
```

Tento příkaz zapíše text "Zpráva" do `soubor1.txt` a `soubor2.txt` současně.

## Tipy
- Používejte možnost `-a`, pokud chcete přidávat data do existujících souborů, abyste neztratili předchozí obsah.
- Můžete kombinovat `tee` s dalšími příkazy pomocí rour, abyste efektivně spravovali výstupy.
- Pokud chcete ignorovat přerušení, použijte možnost `-i`, což může být užitečné při dlouhých operacích.