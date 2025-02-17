# [Linux] Bash exit použití: Ukončení skriptu nebo shellu

## Přehled
Příkaz `exit` se používá k ukončení aktuálního shellu nebo skriptu. Můžete také specifikovat návratový kód, který indikuje úspěšnost nebo neúspěšnost provedení.

## Použití
Základní syntaxe příkazu je následující:

```
exit [možnosti] [návratový_kód]
```

## Běžné možnosti
- `návratový_kód`: Číslo (obvykle mezi 0 a 255), které se vrátí jako výstupní stav. 0 obvykle znamená úspěch, zatímco jakékoliv jiné číslo značí chybu.

## Běžné příklady

### Ukončení skriptu s návratovým kódem 0
```bash
#!/bin/bash
echo "Skript se úspěšně dokončil."
exit 0
```

### Ukončení skriptu s návratovým kódem 1
```bash
#!/bin/bash
echo "Nastala chyba!"
exit 1
```

### Použití exit v interaktivním shellu
```bash
$ echo "Ukončuji shell."
$ exit
```

### Ukončení skriptu s proměnnou jako návratovým kódem
```bash
#!/bin/bash
kód=2
echo "Ukončuji skript s kódem $kód."
exit $kód
```

## Tipy
- Vždy se snažte vracet kód 0 pro úspěšné skripty a jiné hodnoty pro chyby, aby bylo možné snadno diagnostikovat problémy.
- Používejte `exit` na konci skriptu, aby bylo jasné, jaký byl výsledek jeho provedení.
- Pokud skript obsahuje více částí, můžete použít různé návratové kódy pro různé chyby, což usnadní ladění.