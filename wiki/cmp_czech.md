# [Linux] Bash cmp použití: Porovnání dvou souborů

## Overview
Příkaz `cmp` slouží k porovnání dvou souborů byte po bytu. Pokud se soubory liší, `cmp` vypíše první pozici, kde se liší, a také informaci o velikosti souborů. Tento příkaz je užitečný pro rychlé zjištění, zda se dva soubory shodují nebo ne.

## Usage
Základní syntaxe příkazu `cmp` je následující:

```bash
cmp [options] [arguments]
```

## Common Options
- `-l`: Vypíše rozdíly mezi soubory v hexadecimálním formátu.
- `-s`: Zjistí, zda se soubory liší, ale nevypíše žádný výstup.
- `-i OFFSET`: Porovnává soubory od daného offsetu.
- `-n N`: Porovnává pouze prvních N byteů souborů.

## Common Examples
1. Porovnání dvou souborů a zobrazení první odlišnosti:
   ```bash
   cmp file1.txt file2.txt
   ```

2. Použití volby `-s` pro tichou kontrolu shody:
   ```bash
   cmp -s file1.txt file2.txt
   ```

3. Výpis rozdílů v hexadecimálním formátu:
   ```bash
   cmp -l file1.txt file2.txt
   ```

4. Porovnání pouze prvních 100 byteů dvou souborů:
   ```bash
   cmp -n 100 file1.txt file2.txt
   ```

## Tips
- Používejte volbu `-s`, pokud chcete rychle zjistit, zda se soubory liší, aniž byste potřebovali podrobnosti.
- Pokud porovnáváte velké soubory, může být užitečné použít volbu `-n`, abyste omezili porovnání na konkrétní část souboru.
- Příkaz `cmp` je ideální pro binární soubory, protože porovnává data na úrovni byte.