# [Linux] Bash sync použití: Synchronizace dat na disku

## Přehled
Příkaz `sync` slouží k synchronizaci dat mezi pamětí a diskem. Zajišťuje, že všechny změny provedené v souborovém systému jsou uloženy na disk, což pomáhá předcházet ztrátě dat při neočekávaném vypnutí nebo pádu systému.

## Použití
Základní syntaxe příkazu je následující:

```
sync [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Vynutí synchronizaci všech souborů.
- `-d`: Synchronizuje pouze data, nikoli metadata.
- `-n`: Neprovádí synchronizaci, pouze zkontroluje, co by bylo synchronizováno.

## Běžné příklady
1. **Základní použití**:
   Synchronizace všech změn v souborovém systému.
   ```bash
   sync
   ```

2. **Vynucení synchronizace**:
   Vynutí synchronizaci všech souborů.
   ```bash
   sync -f
   ```

3. **Synchronizace dat bez metadat**:
   Synchronizace pouze dat bez aktualizace metadat.
   ```bash
   sync -d
   ```

4. **Kontrola synchronizace**:
   Zkontroluje, co by bylo synchronizováno, aniž by skutečně provedl synchronizaci.
   ```bash
   sync -n
   ```

## Tipy
- Používejte příkaz `sync` před vypnutím systému, abyste zajistili, že všechna data jsou uložena na disku.
- Můžete použít `sync` v kombinaci s jinými příkazy, jako je `cp`, abyste se ujistili, že kopírované soubory jsou správně synchronizovány.
- Pokud pracujete s externími disky, je dobré provést synchronizaci před jejich odpojením.