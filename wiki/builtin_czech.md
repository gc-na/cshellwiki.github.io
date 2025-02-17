# [Linux] Bash builtin příkaz: Zobrazí hodnoty proměnných

## Přehled
Příkaz `builtin` v Bashu slouží k provádění vestavěných příkazů shellu, které by jinak mohly být přepsány externími příkazy. Tento příkaz umožňuje uživatelům explicitně volit vestavěné verze příkazů, což může být užitečné při ladění skriptů nebo při práci s proměnnými.

## Použití
Základní syntaxe příkazu `builtin` je následující:

```bash
builtin [options] [arguments]
```

## Běžné možnosti
- `-p`: Zobrazí pouze vestavěné příkazy.
- `-f`: Použije vestavěnou funkci, pokud je dostupná.

## Běžné příklady
1. **Zobrazení vestavěných příkazů**:
   Chcete-li zobrazit všechny vestavěné příkazy, můžete použít:
   ```bash
   builtin -p
   ```

2. **Spuštění vestavěného příkazu `echo`**:
   Pokud máte externí verzi příkazu `echo`, ale chcete použít vestavěnou, můžete to udělat takto:
   ```bash
   builtin echo "Toto je vestavěný příkaz."
   ```

3. **Použití vestavěné funkce**:
   Pokud máte funkci se stejným názvem jako vestavěný příkaz, můžete ji spustit pomocí:
   ```bash
   builtin my_function
   ```

## Tipy
- Vždy zkontrolujte, zda máte v prostředí definované funkce se stejným názvem jako vestavěné příkazy, abyste předešli nejasnostem.
- Používejte `builtin` v skriptech, kde je důležité zajistit, že se používají vestavěné příkazy, zejména v případech, kdy by externí příkazy mohly způsobit nežádoucí chování.
- Mějte na paměti, že ne všechny příkazy mají vestavěné varianty, takže je dobré se seznámit s dostupnými vestavěnými příkazy ve vašem shellu.