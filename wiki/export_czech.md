# [Linux] Bash export použití: Nastavení proměnných prostředí

## Overview
Příkaz `export` se používá v Bash pro nastavení proměnných prostředí, které jsou dostupné pro všechny podřízené procesy. Pomocí tohoto příkazu můžete sdílet proměnné mezi různými skripty a programy, což je užitečné pro konfiguraci prostředí.

## Usage
Základní syntaxe příkazu `export` je následující:

```bash
export [options] [arguments]
```

## Common Options
- `-p`: Zobrazí všechny exportované proměnné prostředí.
- `-n`: Zruší export proměnné, takže nebude dostupná pro podřízené procesy.

## Common Examples

### Exportování proměnné
Chcete-li exportovat proměnnou, použijte následující příkaz:

```bash
export MY_VAR="Hello, World!"
```

### Zobrazení exportovaných proměnných
Pro zobrazení všech exportovaných proměnných můžete použít:

```bash
export -p
```

### Zrušení exportu proměnné
Pokud chcete zrušit export proměnné, použijte:

```bash
export -n MY_VAR
```

### Použití exportované proměnné v podřízeném procesu
Pokud máte exportovanou proměnnou, můžete ji použít v podřízeném procesu, například v novém shellu:

```bash
export MY_VAR="Hello, World!"
bash -c 'echo $MY_VAR'
```

## Tips
- Vždy se ujistěte, že proměnné, které exportujete, mají správné hodnoty, aby nedošlo k nechtěným chybám v podřízených procesech.
- Používejte `export` na začátku skriptu, pokud potřebujete, aby proměnné byly dostupné pro všechny příkazy ve skriptu.
- Nezapomeňte, že exportované proměnné zůstanou aktivní pouze v aktuální relaci shellu. Po zavření shellu budou ztraceny.