# [Linux] Bash lvm použití: Správa logických svazků

## Přehled
Příkaz `lvm` (Logical Volume Manager) slouží k správě logických svazků v Linuxu. Umožňuje uživatelům vytvářet, měnit a spravovat logické svazky, což usnadňuje manipulaci s diskovým prostorem a zvyšuje flexibilitu správy úložných zařízení.

## Použití
Základní syntaxe příkazu `lvm` je následující:

```
lvm [možnosti] [argumenty]
```

## Běžné možnosti
- `create`: Vytvoří nový logický svazek.
- `remove`: Odstraní existující logický svazek.
- `extend`: Rozšíří existující logický svazek o další prostor.
- `reduce`: Zmenší velikost logického svazku.
- `lvdisplay`: Zobrazí informace o logických svazcích.

## Běžné příklady
1. **Vytvoření nového logického svazku**:
   ```bash
   lvm create -n novy_svazek -L 10G skupina_svazku
   ```

2. **Odstranění logického svazku**:
   ```bash
   lvm remove novy_svazek
   ```

3. **Rozšíření logického svazku**:
   ```bash
   lvm extend -L +5G novy_svazek
   ```

4. **Zmenšení logického svazku**:
   ```bash
   lvm reduce -L -3G novy_svazek
   ```

5. **Zobrazení informací o logických svazcích**:
   ```bash
   lvm lvdisplay
   ```

## Tipy
- Před prováděním operací na logických svazcích vždy zálohujte důležitá data.
- Používejte příkaz `lvdisplay` k ověření stavu logických svazků před a po provedení změn.
- Při rozšiřování logických svazků se ujistěte, že máte dostatek volného místa na fyzických svazcích.