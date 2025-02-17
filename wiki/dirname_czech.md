# [Linux] Bash dirname použití: Získání názvu adresáře souboru

## Overview
Příkaz `dirname` slouží k extrakci názvu adresáře z cesty k souboru. Vrací část cesty, která obsahuje pouze adresář, a ignoruje název souboru.

## Usage
Základní syntaxe příkazu je následující:

```
dirname [options] [arguments]
```

## Common Options
- `-z`, `--zero`: Odděluje vstupní cesty nulovými bajty místo nových řádků, což je užitečné pro zpracování cest obsahujících mezery.
- `--help`: Zobrazí nápovědu k použití příkazu.
- `--version`: Zobrazí verzi příkazu.

## Common Examples
1. Získání názvu adresáře z cesty k souboru:
   ```bash
   dirname /home/user/documents/file.txt
   ```
   Výstup: `/home/user/documents`

2. Získání názvu adresáře z cesty s koncovým lomítkem:
   ```bash
   dirname /home/user/documents/
   ```
   Výstup: `/home/user/documents`

3. Zpracování více cest najednou:
   ```bash
   dirname /home/user/file1.txt /home/user/documents/file2.txt
   ```
   Výstup:
   ```
   /home/user
   /home/user/documents
   ```

4. Použití s nulovými bajty:
   ```bash
   printf "/home/user/file1.txt\0/home/user/documents/file2.txt\0" | dirname -z
   ```
   Výstup:
   ```
   /home/user
   /home/user/documents
   ```

## Tips
- Při práci s cestami, které obsahují mezery, je dobré použít uvozovky, aby se předešlo chybám.
- `dirname` je užitečný v skriptech pro zpracování cest a automatizaci úloh, kde potřebujete oddělit názvy souborů od jejich adresářů.