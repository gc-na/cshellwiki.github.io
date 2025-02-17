# [Linux] Bash update-rc.d použití: Správa skriptů při spouštění

## Přehled
Příkaz `update-rc.d` slouží k přidávání, odstraňování nebo aktualizaci skriptů, které se spouštějí při startu nebo vypnutí systému. Tento nástroj je užitečný pro správu služeb a demonstruje, jakým způsobem se skripty integrují do systému init.

## Použití
Základní syntaxe příkazu je následující:

```bash
update-rc.d [možnosti] [argumenty]
```

## Běžné možnosti
- `defaults`: Přidá skript do výchozích runlevelů.
- `remove`: Odstraní skript ze všech runlevelů.
- `enable`: Povolí skript pro automatické spouštění.
- `disable`: Zakáže skript pro automatické spouštění.

## Běžné příklady
Přidání skriptu do výchozích runlevelů:

```bash
sudo update-rc.d myscript defaults
```

Odstranění skriptu ze všech runlevelů:

```bash
sudo update-rc.d myscript remove
```

Povolení skriptu pro automatické spouštění:

```bash
sudo update-rc.d myscript enable
```

Zakázání skriptu pro automatické spouštění:

```bash
sudo update-rc.d myscript disable
```

## Tipy
- Před provedením změn vždy zálohujte své skripty, abyste se vyhnuli ztrátě dat.
- Ujistěte se, že skripty mají správná oprávnění pro spuštění.
- Používejte `update-rc.d` s opatrností, zejména na produkčních serverech, abyste předešli nechtěnému zastavení služeb.