# [Linux] Bash watch použití: Sledujte příkazy v reálném čase

## Přehled
Příkaz `watch` slouží k pravidelnému spouštění jiného příkazu a zobrazení jeho výstupu na obrazovce. To je užitečné pro sledování změn v reálném čase, například pro monitorování systémových zdrojů nebo souborů.

## Použití
Základní syntaxe příkazu `watch` je následující:

```bash
watch [možnosti] [argumenty]
```

## Běžné možnosti
- `-n [sekundy]`: Určuje interval (v sekundách) mezi jednotlivými spuštěními příkazu. Výchozí hodnota je 2 sekundy.
- `-d`: Zvýrazní změny mezi jednotlivými výstupy.
- `-t`: Skryje hlavičku, která zobrazuje čas a interval.
- `-x`: Spustí příkaz s argumenty, které jsou předány jako příkazový řádek.

## Běžné příklady
Sledování využití procesoru pomocí příkazu `top`:

```bash
watch -n 1 top
```

Sledování obsahu adresáře:

```bash
watch -d ls -l
```

Sledování změn v souboru pomocí příkazu `cat`:

```bash
watch -n 5 cat /path/to/file.txt
```

Sledování využití disku pomocí příkazu `df`:

```bash
watch -n 10 df -h
```

## Tipy
- Používejte možnost `-d`, pokud chcete snadno vidět změny mezi jednotlivými výstupy.
- Zvažte nastavení delšího intervalu pomocí `-n`, pokud sledujete příkaz, který se mění méně často, abyste ušetřili systémové zdroje.
- Pokud chcete sledovat více příkazů, můžete použít `watch` v kombinaci s příkazem `bash`, například:

```bash
watch -n 2 'df -h; free -m'
```

Tímto způsobem můžete efektivně sledovat různé aspekty systému v reálném čase.