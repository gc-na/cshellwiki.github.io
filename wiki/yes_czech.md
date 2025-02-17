# [Linux] Bash yes použití: Opakování textu

## Přehled
Příkaz `yes` v Bash slouží k neustálému opakování zadaného textu. Nejčastěji se používá k automatizaci odpovědí na dotazy, které vyžadují potvrzení, například při instalaci softwaru.

## Použití
Základní syntaxe příkazu `yes` je následující:

```bash
yes [options] [arguments]
```

## Běžné možnosti
- `-n`, `--no-newline`: Nezahrnuje nový řádek na konci výstupu.
- `-h`, `--help`: Zobrazí nápovědu k příkazu.
- `-V`, `--version`: Zobrazí verzi příkazu.

## Běžné příklady
1. **Základní použití**: Opakování slova "ano" nekonečně.
   ```bash
   yes
   ```

2. **Opakování vlastního textu**: Opakování slova "pokračovat".
   ```bash
   yes pokračovat
   ```

3. **Použití s instalací**: Automatické potvrzení během instalace.
   ```bash
   yes | sudo apt install balíček
   ```

4. **Bez nového řádku**: Opakování textu bez nového řádku.
   ```bash
   yes -n "potvrzuji" | head -n 5
   ```

## Tipy
- Používejte `yes` v kombinaci s příkazy, které vyžadují interakci, abyste urychlili proces.
- Buďte opatrní při používání `yes` s příkazy, které mohou mít destruktivní účinky, protože automaticky potvrzuje všechny dotazy.