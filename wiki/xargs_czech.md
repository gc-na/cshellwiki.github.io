# [Linux] Bash xargs Použití: Zpracování vstupu z příkazového řádku

## Přehled
Příkaz `xargs` slouží k převodu vstupu z příkazového řádku na argumenty pro jiný příkaz. Umožňuje efektivně zpracovávat velké množství dat, které by jinak nebylo možné předat přímo jako argumenty.

## Použití
Základní syntaxe příkazu `xargs` je následující:

```bash
xargs [možnosti] [argumenty]
```

## Běžné možnosti
- `-n N`: Určuje maximální počet argumentů, které budou předány jednomu příkazu.
- `-d DELIM`: Určuje oddělovač pro vstupní data (výchozí je mezera).
- `-0`: Očekává, že vstup bude ukončen nulovým znakem (užitečné pro zpracování souborů s mezerami v názvech).
- `-p`: Před každým provedením příkazu se zeptá na potvrzení.

## Běžné příklady
1. **Základní použití s `echo`:**
   ```bash
   echo "a b c" | xargs mkdir
   ```
   Tento příkaz vytvoří adresáře `a`, `b` a `c`.

2. **Použití s `find`:**
   ```bash
   find . -name "*.txt" | xargs rm
   ```
   Tento příkaz najde všechny soubory s příponou `.txt` a odstraní je.

3. **Omezení počtu argumentů:**
   ```bash
   echo "1 2 3 4 5" | xargs -n 2 echo
   ```
   Tento příkaz vypíše `1 2`, `3 4`, a `5` na nových řádcích.

4. **Použití s nulovými oddělovači:**
   ```bash
   find . -name "*.txt" -print0 | xargs -0 rm
   ```
   Tento příkaz odstraní soubory s příponou `.txt`, přičemž správně zpracovává názvy souborů obsahující mezery.

## Tipy
- Při práci s velkým množstvím dat je dobré použít `-n` pro omezení počtu argumentů, aby se předešlo chybám.
- Používejte `-0` s příkazy, které generují výstup s nulovými oddělovači, aby se zajistilo správné zpracování názvů souborů.
- Před provedením destruktivních operací, jako je `rm`, je dobré použít `-p` pro potvrzení, aby se předešlo nechtěnému smazání souborů.