# [Linux] Bash lvs použití: Zobrazování logických svazků

## Přehled
Příkaz `lvs` slouží k zobrazení informací o logických svazcích v systému správy svazků LVM (Logical Volume Manager). Umožňuje uživatelům snadno sledovat a spravovat logické svazky.

## Použití
Základní syntaxe příkazu `lvs` je následující:

```bash
lvs [možnosti] [argumenty]
```

## Běžné možnosti
- `-o` : Určuje, které sloupce se mají zobrazit.
- `-a` : Zobrazí všechny logické svazky, včetně skrytých.
- `-n` : Zobrazí pouze logické svazky s daným názvem.
- `--units` : Umožňuje specifikovat jednotky pro zobrazení velikostí.

## Běžné příklady
1. Zobrazení všech logických svazků:
   ```bash
   lvs
   ```

2. Zobrazení podrobností o konkrétním logickém svazku:
   ```bash
   lvs -o +devices
   ```

3. Zobrazení všech logických svazků včetně skrytých:
   ```bash
   lvs -a
   ```

4. Zobrazení logických svazků s konkrétními sloupci:
   ```bash
   lvs -o lv_name,lv_size
   ```

5. Zobrazení logických svazků s velikostmi v megabajtech:
   ```bash
   lvs --units m
   ```

## Tipy
- Při použití `lvs` s volbou `-o` můžete přizpůsobit zobrazení podle svých potřeb a zaměřit se na relevantní informace.
- Pokud pracujete s více logickými svazky, zvažte použití skriptů pro automatizaci pravidelných kontrol.
- Nezapomeňte, že příkaz `lvs` vyžaduje oprávnění pro přístup k informacím o svazcích, takže je dobré ho spouštět s příslušnými právy.