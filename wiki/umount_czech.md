# [Linux] Bash umount použití: Odpojení souborového systému

## Přehled
Příkaz `umount` slouží k odpojení souborového systému od jeho připojeného místa v systému. To je užitečné, když chcete bezpečně odstranit externí zařízení, jako jsou USB disky nebo síťové svazky, a zajistit, že všechny změny byly uloženy a žádné procesy nepracují se soubory na tomto zařízení.

## Použití
Základní syntaxe příkazu `umount` je následující:

```
umount [možnosti] [argumenty]
```

## Běžné možnosti
- `-a`: Odpojí všechny souborové systémy uvedené v `/etc/mtab`.
- `-f`: Vynutí odpojení souborového systému, i když je stále používán.
- `-l`: Odpojí souborový systém "lazy", což znamená, že se odpojení provede, jakmile nebude souborový systém používán.
- `-r`: Pokusí se automaticky opravit souborový systém, pokud je připojený a došlo k chybě.

## Běžné příklady
1. **Odpojení USB disku podle cesty:**
   ```bash
   umount /media/usb
   ```

2. **Odpojení USB disku podle zařízení:**
   ```bash
   umount /dev/sdb1
   ```

3. **Vynucené odpojení souborového systému:**
   ```bash
   umount -f /media/usb
   ```

4. **Lazy odpojení souborového systému:**
   ```bash
   umount -l /media/usb
   ```

5. **Odpojení všech souborových systémů uvedených v `/etc/mtab`:**
   ```bash
   umount -a
   ```

## Tipy
- Před odpojením souborového systému se ujistěte, že na něm nejsou otevřené soubory nebo běžící procesy, aby se předešlo ztrátě dat.
- Použití volby `-l` může být užitečné, pokud potřebujete odpojit souborový systém, ale procesy na něm stále běží.
- Vždy se ujistěte, že jste na správném připojeném bodě nebo zařízení, abyste se vyhnuli nechtěnému odpojení důležitých souborových systémů.