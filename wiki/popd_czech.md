# [Linux] Bash popd použití: Odstranění adresáře ze zásobníku

## Přehled
Příkaz `popd` se používá k odstranění adresáře z zásobníku pracovních adresářů. Tento příkaz je užitečný při navigaci mezi různými adresáři v terminálu, zejména když používáte příkaz `pushd`, který přidává adresáře do zásobníku.

## Použití
Základní syntaxe příkazu `popd` je následující:

```bash
popd [options] [arguments]
```

## Běžné možnosti
- `-n`: Neprovádí změnu pracovního adresáře, pouze odstraní adresář ze zásobníku.
- `+n`: Odstraní adresář na pozici `n` v zásobníku, místo posledního adresáře.

## Běžné příklady
1. **Základní použití**:
   Odstranění posledního přidaného adresáře ze zásobníku.
   ```bash
   popd
   ```

2. **Použití s možností -n**:
   Odstranění adresáře ze zásobníku bez změny pracovního adresáře.
   ```bash
   popd -n
   ```

3. **Odstranění adresáře na specifické pozici**:
   Odstranění adresáře na druhé pozici v zásobníku.
   ```bash
   popd +1
   ```

## Tipy
- Před použitím `popd` se ujistěte, že máte v zásobníku adresáře, jinak příkaz nebude mít žádný efekt.
- Používejte `pushd` a `popd` společně pro efektivní správu pracovních adresářů.
- Můžete si zkontrolovat aktuální stav zásobníku pomocí příkazu `dirs`, který zobrazí seznam adresářů v zásobníku.