# [Linux] Bash wait použití: Čekání na dokončení procesů

## Přehled
Příkaz `wait` v Bash slouží k pozastavení vykonávání skriptu, dokud nedokončí všechny pozadí běžící procesy. Je užitečný, když potřebujete zajistit, aby se další příkazy vykonaly až po dokončení předchozích úloh.

## Použití
Základní syntaxe příkazu `wait` je následující:

```
wait [options] [arguments]
```

## Běžné možnosti
- `-n`: Čeká na dokončení jakéhokoli procesu na pozadí.
- `-p`: Čeká na konkrétní PID procesu.
- `PID`: Číslo procesu, na který chcete čekat.

## Běžné příklady

### Čekání na všechny procesy na pozadí
```bash
sleep 5 &
sleep 3 &
wait
echo "Všechny procesy na pozadí byly dokončeny."
```

### Čekání na konkrétní proces
```bash
sleep 5 &
PID=$!
echo "Čekám na proces s PID: $PID"
wait $PID
echo "Proces s PID: $PID byl dokončen."
```

### Čekání na první dokončený proces
```bash
sleep 5 &
sleep 3 &
wait -n
echo "První proces na pozadí byl dokončen."
```

## Tipy
- Používejte `wait` v kombinaci s procesy na pozadí, abyste efektivně spravovali běh skriptů.
- Pokud potřebujete sledovat více procesů, můžete uložit jejich PID do pole a poté použít `wait` pro každé PID.
- Vždy zkontrolujte, zda procesy na pozadí skutečně běží, abyste se vyhnuli zbytečnému čekání.