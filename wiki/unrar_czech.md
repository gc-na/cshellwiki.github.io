# [Linux] Bash unrar použití: Extrakce souborů RAR

## Přehled
Příkaz `unrar` slouží k extrakci souborů ze souborů RAR. Tento nástroj je užitečný pro práci s archivovanými daty, která jsou komprimována do formátu RAR, a umožňuje uživatelům snadno získat přístup k obsahu těchto archivů.

## Použití
Základní syntaxe příkazu `unrar` je následující:

```bash
unrar [možnosti] [argumenty]
```

## Běžné možnosti
- `x` - Extrakce souborů s úplnou cestou.
- `e` - Extrakce souborů do aktuálního adresáře bez zachování struktury adresářů.
- `l` - Zobrazení seznamu souborů v archivu.
- `t` - Ověření integrity archivu.
- `v` - Zobrazení podrobného výstupu během extrakce.

## Běžné příklady
- Extrakce všech souborů z archivu do aktuálního adresáře:
  ```bash
  unrar x archiv.rar
  ```

- Extrakce souborů do specifikovaného adresáře:
  ```bash
  unrar x archiv.rar /cesta/k/adresari/
  ```

- Zobrazení seznamu souborů v archivu:
  ```bash
  unrar l archiv.rar
  ```

- Ověření integrity archivu:
  ```bash
  unrar t archiv.rar
  ```

- Extrakce souborů bez zachování struktury adresářů:
  ```bash
  unrar e archiv.rar
  ```

## Tipy
- Před extrakcí souborů je dobré ověřit integritu archivu pomocí možnosti `t`, aby se zajistilo, že není poškozený.
- Pokud pracujete s velkými archivy, použijte možnost `v` pro podrobnější výstup, což vám pomůže sledovat průběh extrakce.
- Ujistěte se, že máte dostatek místa na disku pro extrakci souborů, zejména pokud pracujete s velkými RAR archivy.