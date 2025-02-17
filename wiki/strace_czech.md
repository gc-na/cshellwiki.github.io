# [Linux] Bash strace použití: Nástroj pro sledování systémových volání

## Přehled
Příkaz `strace` slouží k sledování systémových volání a signálů, které provádí běžící proces. Pomocí `strace` můžete diagnostikovat problémy s aplikacemi, sledovat interakce s jádrem operačního systému a analyzovat chování programů.

## Použití
Základní syntaxe příkazu `strace` je následující:

```
strace [možnosti] [argumenty]
```

## Běžné možnosti
- `-e trace=<typ>`: Sledování pouze specifikovaných systémových volání (např. `-e trace=open`).
- `-o <soubor>`: Uložení výstupu do souboru místo na standardní výstup.
- `-p <PID>`: Sledování již běžícího procesu podle jeho PID.
- `-c`: Shrnutí počtu systémových volání a jejich časů.
- `-f`: Sledování procesů, které jsou vytvořeny pomocí `fork`.

## Běžné příklady
Sledování konkrétního příkazu:

```bash
strace ls
```

Sledování systému volání pro otevření souboru:

```bash
strace -e trace=open ./my_program
```

Uložení výstupu do souboru:

```bash
strace -o output.txt ./my_program
```

Sledování běžícího procesu podle PID:

```bash
strace -p 1234
```

Shrnutí systémových volání:

```bash
strace -c ./my_program
```

## Tipy
- Používejte `-o` pro ukládání výstupu do souboru, abyste mohli snadno analyzovat výsledky později.
- Kombinujte `-e trace` s dalšími možnostmi pro cílené sledování.
- Při sledování procesů s vysokou aktivitou buďte opatrní, protože `strace` může ovlivnit výkon aplikace.