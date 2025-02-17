# [Linux] Bash resize2fs použití: Změna velikosti souborového systému ext2/ext3/ext4

## Přehled
Příkaz `resize2fs` slouží k změně velikosti souborového systému na diskových oddílech, které používají formáty ext2, ext3 nebo ext4. Umožňuje zvětšit nebo zmenšit velikost souborového systému podle aktuálních potřeb.

## Použití
Základní syntaxe příkazu je následující:

```bash
resize2fs [možnosti] [argumenty]
```

## Běžné možnosti
- `-f`: Vynutí změnu velikosti souborového systému, i když není nutná.
- `-p`: Zobrazí průběh operace.
- `-s`: Změní velikost souborového systému na velikost oddílu.
- `-M`: Zmenší souborový systém na minimum.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `resize2fs`:

### Zvětšení souborového systému
Pokud chcete zvětšit souborový systém na oddílu `/dev/sda1` na maximální velikost, použijte:

```bash
resize2fs /dev/sda1
```

### Zmenšení souborového systému
Pro zmenšení souborového systému na oddílu `/dev/sda1` na velikost 20 GB:

```bash
resize2fs /dev/sda1 20G
```

### Vynucení změny velikosti
Pokud potřebujete vynutit změnu velikosti souborového systému, použijte:

```bash
resize2fs -f /dev/sda1
```

### Zobrazení průběhu
Chcete-li vidět průběh operace při zvětšování souborového systému, použijte:

```bash
resize2fs -p /dev/sda1
```

## Tipy
- Před provedením změny velikosti souborového systému vždy zálohujte důležitá data.
- Ujistěte se, že je souborový systém odpojený, pokud provádíte zmenšení velikosti.
- Před zmenšením souborového systému zkontrolujte jeho integritu pomocí příkazu `e2fsck`.