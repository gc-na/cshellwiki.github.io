# [Linux] Bash rm Použití: Odstranění souborů a adresářů

## Přehled
Příkaz `rm` slouží k odstranění souborů a adresářů v systému Linux. Je to mocný nástroj, který umožňuje uživatelům trvale vymazat soubory z jejich systému.

## Použití
Základní syntaxe příkazu `rm` je následující:

```bash
rm [možnosti] [argumenty]
```

## Běžné možnosti
- `-f` : Vynucené odstranění souborů bez potvrzení.
- `-i` : Interaktivní režim, který vyžaduje potvrzení před odstraněním každého souboru.
- `-r` : Odstranění adresářů a jejich obsahu rekurzivně.
- `-v` : Verbózní režim, který zobrazuje podrobnosti o odstraněných souborech.

## Běžné příklady
1. Odstranění jednoho souboru:
   ```bash
   rm soubor.txt
   ```

2. Odstranění více souborů najednou:
   ```bash
   rm soubor1.txt soubor2.txt soubor3.txt
   ```

3. Odstranění adresáře a jeho obsahu rekurzivně:
   ```bash
   rm -r adresar/
   ```

4. Vynucené odstranění souboru bez potvrzení:
   ```bash
   rm -f soubor.txt
   ```

5. Interaktivní odstranění souboru:
   ```bash
   rm -i soubor.txt
   ```

## Tipy
- Vždy buďte opatrní při používání příkazu `rm`, zejména s možností `-r`, protože odstraněné soubory nelze obnovit.
- Doporučuje se používat možnost `-i`, pokud si nejste jisti, zda chcete soubory skutečně odstranit.
- Před odstraněním důležitých souborů si je zálohujte, abyste předešli nechtěné ztrátě dat.