# [Linux] Bash uname použití: Získání informací o systému

## Přehled
Příkaz `uname` slouží k získání informací o operačním systému a hardwarové architektuře. Může poskytnout různé detaily, jako je název jádra, verze jádra a typ stroje.

## Použití
Základní syntaxe příkazu je následující:
```
uname [možnosti]
```

## Běžné možnosti
- `-a`: Zobrazí všechny dostupné informace o systému.
- `-s`: Zobrazí název jádra.
- `-n`: Zobrazí název hostitele.
- `-r`: Zobrazí verzi jádra.
- `-v`: Zobrazí datum a čas kompilace jádra.
- `-m`: Zobrazí architekturu stroje.
- `-o`: Zobrazí název operačního systému.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `uname`:

1. Zobrazit všechny informace o systému:
   ```bash
   uname -a
   ```

2. Zobrazit pouze název jádra:
   ```bash
   uname -s
   ```

3. Zobrazit verzi jádra:
   ```bash
   uname -r
   ```

4. Zobrazit architekturu stroje:
   ```bash
   uname -m
   ```

5. Zobrazit název operačního systému:
   ```bash
   uname -o
   ```

## Tipy
- Použití `uname -a` je užitečné pro rychlé získání všech informací o systému v jednom příkazu.
- Pokud potřebujete specifické informace, použijte jednotlivé možnosti, abyste získali přesně to, co potřebujete.
- Tento příkaz je často používán při diagnostice problémů se systémem nebo při přípravě na instalaci softwaru, který závisí na specifických vlastnostech systému.