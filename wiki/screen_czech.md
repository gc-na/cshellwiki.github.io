# [Linux] Bash screen použití: Správa více terminálů

## Přehled
Příkaz `screen` slouží k vytváření a správě virtuálních terminálů v systému Linux. Umožňuje uživatelům spouštět více shellů v jednom okně a přepínat mezi nimi, což je užitečné pro multitasking a práci na vzdálených serverech.

## Použití
Základní syntaxe příkazu `screen` je následující:

```
screen [možnosti] [argumenty]
```

## Běžné možnosti
- `-S <název>`: Pojmenuje novou relaci.
- `-d -r <název>`: Odpojí a znovu připojí k existující relaci.
- `-list`: Zobrazí seznam všech běžících relací.
- `-x`: Připojí se k existující relaci v režimu sdílení.

## Běžné příklady
1. **Vytvoření nové relace:**
   ```bash
   screen
   ```

2. **Pojmenování relace:**
   ```bash
   screen -S moje_relace
   ```

3. **Odpojení od relace:**
   Stiskněte `Ctrl + A`, poté `D`.

4. **Zobrazení seznamu relací:**
   ```bash
   screen -list
   ```

5. **Připojení k existující relaci:**
   ```bash
   screen -r moje_relace
   ```

6. **Připojení k relaci v režimu sdílení:**
   ```bash
   screen -x moje_relace
   ```

## Tipy
- Používejte pojmenované relace, abyste se snadno orientovali mezi více relacemi.
- Pravidelně kontrolujte seznam relací pomocí `screen -list`, abyste se ujistili, že máte přehled o běžících procesech.
- Pokud pracujete na vzdáleném serveru, můžete relaci `screen` odpojit a později se k ní znovu připojit, což je velmi užitečné pro dlouhotrvající úlohy.