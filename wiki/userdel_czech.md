# [Linux] Bash userdel použití: Odstranění uživatelského účtu

## Přehled
Příkaz `userdel` se používá k odstranění uživatelského účtu ze systému. Tento příkaz může být užitečný v situacích, kdy je třeba odstranit uživatele, který již není potřebný, nebo když se provádí údržba systému.

## Použití
Základní syntaxe příkazu `userdel` je následující:

```
userdel [možnosti] [uživatelské jméno]
```

## Běžné možnosti
- `-r`: Odstraní domovský adresář uživatele a jeho obsah.
- `-f`: Vynutí odstranění uživatele, i když je přihlášen.
- `-h`: Zobrazí nápovědu k příkazu.

## Běžné příklady
1. Odstranění uživatelského účtu bez odstranění domovského adresáře:
   ```bash
   userdel janek
   ```

2. Odstranění uživatelského účtu včetně domovského adresáře:
   ```bash
   userdel -r janek
   ```

3. Vynucení odstranění uživatelského účtu, i když je uživatel přihlášen:
   ```bash
   userdel -f janek
   ```

## Tipy
- Před odstraněním uživatelského účtu se ujistěte, že uživatel není přihlášen, aby se předešlo problémům.
- Používejte možnost `-r` opatrně, protože odstraní všechny související soubory a adresáře.
- Doporučuje se provést zálohu důležitých dat před odstraněním uživatelského účtu.