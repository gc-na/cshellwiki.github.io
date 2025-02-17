# [Linux] Bash dirs použití: Zobrazí seznam adresářů v zásobníku

## Přehled
Příkaz `dirs` v Bash slouží k zobrazení seznamu adresářů, které jsou uloženy v zásobníku aktuálního shellu. Tento příkaz je užitečný pro správu a navigaci mezi různými adresáři, které jste navštívili v rámci aktuální relace.

## Použití
Základní syntaxe příkazu `dirs` je následující:

```
dirs [options] [arguments]
```

## Běžné možnosti
- `-l`: Zobrazí seznam adresářů v dlouhém formátu.
- `-p`: Zobrazí adresáře v "položkovém" formátu, což znamená, že každý adresář bude na novém řádku.
- `+N`: Zobrazí adresáře začínající od indexu N.
- `-N`: Zobrazí adresáře začínající od konce zásobníku.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `dirs`:

1. **Zobrazení aktuálního seznamu adresářů:**
   ```bash
   dirs
   ```

2. **Zobrazení adresářů v dlouhém formátu:**
   ```bash
   dirs -l
   ```

3. **Zobrazení adresářů v položkovém formátu:**
   ```bash
   dirs -p
   ```

4. **Zobrazení adresáře na indexu 1:**
   ```bash
   dirs +1
   ```

5. **Zobrazení posledního adresáře v zásobníku:**
   ```bash
   dirs -1
   ```

## Tipy
- Používejte příkaz `pushd` a `popd` spolu s `dirs` pro efektivní správu adresářů v zásobníku.
- Můžete kombinovat `dirs` s dalšími příkazy, jako je `echo`, pro lepší přehlednost.
- Pokud často přepínáte mezi několika adresáři, zvažte vytvoření aliasů pro rychlejší přístup.