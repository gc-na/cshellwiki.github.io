# [Linux] Bash ss použití: Zobrazování socketů a jejich stavu

## Přehled
Příkaz `ss` slouží k zobrazení informací o síťových socketech na systému. Je to modernější a rychlejší alternativa k příkazu `netstat`, který se používá k monitorování síťových připojení, portů a dalších síťových statistik.

## Použití
Základní syntaxe příkazu `ss` je následující:

```bash
ss [možnosti] [argumenty]
```

## Běžné možnosti
- `-t`: Zobrazí pouze TCP sockety.
- `-u`: Zobrazí pouze UDP sockety.
- `-l`: Zobrazí pouze naslouchající sockety.
- `-p`: Zobrazí procesy, které používají sockety.
- `-n`: Zobrazí čísla portů místo názvů služeb.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `ss`:

### Zobrazit všechny sockety
```bash
ss -a
```

### Zobrazit pouze TCP sockety
```bash
ss -t
```

### Zobrazit naslouchající sockety
```bash
ss -l
```

### Zobrazit sockety s procesy
```bash
ss -p
```

### Zobrazit UDP sockety
```bash
ss -u
```

### Zobrazit sockety s čísly portů
```bash
ss -n
```

## Tipy
- Používejte kombinaci možností pro získání specifických informací, například `ss -tunlp` pro zobrazení všech TCP a UDP socketů s procesy.
- Příkaz `ss` je rychlejší než `netstat`, takže je vhodné ho používat pro rychlou diagnostiku síťových problémů.
- Pokud potřebujete více informací o konkrétním socketu, můžete použít příkaz `ss -i` pro zobrazení podrobností o socketu.