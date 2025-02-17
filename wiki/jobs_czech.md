# [Linux] Bash jobs použití: Zobrazit běžící úlohy

## Overview
Příkaz `jobs` v Bash slouží k zobrazení seznamu úloh, které běží na pozadí nebo jsou pozastavené v aktuálním shellu. Umožňuje uživatelům sledovat stav těchto úloh a efektivně s nimi manipulovat.

## Usage
Základní syntaxe příkazu `jobs` je následující:

```bash
jobs [options] [arguments]
```

## Common Options
- `-l`: Zobrazí PID (identifikátor procesu) každé úlohy.
- `-n`: Zobrazí pouze úlohy, které se změnily od posledního volání příkazu.
- `-p`: Zobrazí pouze PID úloh.

## Common Examples
Zde je několik praktických příkladů použití příkazu `jobs`:

1. Zobrazení všech běžících a pozastavených úloh:
   ```bash
   jobs
   ```

2. Zobrazení úloh s PID:
   ```bash
   jobs -l
   ```

3. Zobrazení pouze úloh, které se změnily:
   ```bash
   jobs -n
   ```

4. Zobrazení pouze PID úloh:
   ```bash
   jobs -p
   ```

## Tips
- Pokud chcete obnovit pozastavenou úlohu, můžete použít příkaz `fg` následovaný číslem úlohy, například `fg %1` pro obnovení první úlohy.
- Ujistěte se, že pravidelně kontrolujete úlohy na pozadí, abyste měli přehled o tom, co běží a co je pozastaveno.
- Použijte příkaz `bg` pro obnovení pozastavené úlohy na pozadí, což umožní pokračovat v práci v shellu.