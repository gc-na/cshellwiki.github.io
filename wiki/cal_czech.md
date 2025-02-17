# [Linux] Bash cal použití: Zobrazí kalendář

## Přehled
Příkaz `cal` slouží k zobrazení kalendáře pro aktuální měsíc nebo pro jiný specifikovaný měsíc a rok. Je to jednoduchý nástroj, který umožňuje rychlý přehled o datech.

## Použití
Základní syntaxe příkazu je následující:

```bash
cal [možnost] [argumenty]
```

## Běžné možnosti
- `-m` : Zobrazí kalendář pro aktuální měsíc.
- `-y` : Zobrazí kalendář pro celý aktuální rok.
- `-3` : Zobrazí kalendář pro aktuální měsíc a měsíc před a po.
- `-j` : Zobrazí kalendář s dny v roce.
- `-A [n]` : Zobrazí kalendář pro následujících `n` měsíců.
- `-B [n]` : Zobrazí kalendář pro předchozích `n` měsíců.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `cal`:

1. Zobrazení kalendáře pro aktuální měsíc:
   ```bash
   cal
   ```

2. Zobrazení kalendáře pro konkrétní měsíc a rok (např. březen 2023):
   ```bash
   cal 3 2023
   ```

3. Zobrazení kalendáře pro celý aktuální rok:
   ```bash
   cal -y
   ```

4. Zobrazení kalendáře pro aktuální měsíc a dva měsíce před a po:
   ```bash
   cal -3
   ```

5. Zobrazení kalendáře s dny v roce:
   ```bash
   cal -j
   ```

## Tipy
- Pokud často potřebujete kalendář pro různé měsíce, můžete si vytvořit alias pro příkaz s vašimi oblíbenými možnostmi.
- Používejte možnost `-A` a `-B` pro rychlé zobrazení kalendáře pro více měsíců najednou.
- Zvažte použití příkazu `ncal`, který nabízí alternativní zobrazení kalendáře s dalšími funkcemi.