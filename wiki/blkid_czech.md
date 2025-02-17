# [Linux] Bash blkid použití: Získání informací o blokových zařízeních

## Přehled
Příkaz `blkid` slouží k zobrazení informací o blokových zařízeních v systému. Umožňuje uživatelům získat detaily jako UUID, typ souborového systému a další metadata o připojených diskových oddílech.

## Použití
Základní syntaxe příkazu je následující:

```bash
blkid [options] [arguments]
```

## Běžné možnosti
- `-o` : Určuje formát výstupu (např. `value`, `full`).
- `-s` : Specifikuje, které atributy se mají zobrazit (např. `UUID`, `TYPE`).
- `-p` : Zahrnuje informace o zařízení, které nejsou připojené.
- `-c` : Používá cache pro zrychlení dotazu.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `blkid`:

### Zobrazení všech blokových zařízení
```bash
blkid
```

### Získání UUID konkrétního zařízení
```bash
blkid /dev/sda1
```

### Zobrazení pouze UUID a typu souborového systému
```bash
blkid -s UUID -s TYPE
```

### Použití cache pro rychlejší dotaz
```bash
blkid -c /dev/null
```

## Tipy
- Používejte `blkid` bez argumentů pro rychlý přehled všech blokových zařízení v systému.
- Pokud potřebujete specifické informace, využijte možnosti `-s` k zobrazení pouze požadovaných atributů.
- Pro skripty je užitečné použít `-o value`, aby se získal čistý výstup bez dalších informací.