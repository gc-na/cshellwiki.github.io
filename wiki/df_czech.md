# [Linux] Bash df použití: Zobrazení dostupného místa na disku

## Přehled
Příkaz `df` slouží k zobrazení informací o dostupném a využitém místě na diskových oddílech. Umožňuje uživatelům rychle zjistit, kolik místa je na jednotlivých souborových systémech k dispozici.

## Použití
Základní syntaxe příkazu je následující:

```bash
df [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Zobrazí velikosti v lidsky čitelném formátu (např. KB, MB, GB).
- `-T`: Zobrazí typ souborového systému.
- `-a`: Zobrazí všechny souborové systémy, včetně těch, které mají 0 bloků.
- `-i`: Zobrazí informace o inodech místo bloků.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `df`:

1. Zobrazení dostupného místa na všech připojených souborových systémech:
    ```bash
    df
    ```

2. Zobrazení informací v lidsky čitelném formátu:
    ```bash
    df -h
    ```

3. Zobrazení typů souborových systémů:
    ```bash
    df -T
    ```

4. Zobrazení informací o inodech:
    ```bash
    df -i
    ```

5. Zobrazení všech souborových systémů, včetně těch s 0 bloky:
    ```bash
    df -a
    ```

## Tipy
- Používejte možnost `-h`, abyste snadno porozuměli velikostem diskového prostoru.
- Pravidelně kontrolujte dostupné místo, abyste předešli problémům s nedostatkem místa na disku.
- Můžete kombinovat více možností, například `df -hT`, abyste získali více informací najednou.