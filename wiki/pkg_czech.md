# [Linux] Bash pkg použití: Správa balíčků

## Přehled
Příkaz `pkg` slouží k správě balíčků v operačních systémech, které jej podporují. Umožňuje uživatelům instalovat, aktualizovat a odstraňovat software, což usnadňuje správu aplikací a knihoven.

## Použití
Základní syntaxe příkazu `pkg` je následující:

```
pkg [možnosti] [argumenty]
```

## Běžné možnosti
- `install`: Nainstaluje zadaný balíček.
- `remove`: Odstraní zadaný balíček.
- `update`: Aktualizuje seznam dostupných balíčků.
- `upgrade`: Aktualizuje nainstalované balíčky na nejnovější verze.
- `search`: Hledá balíčky podle zadaného názvu nebo klíčového slova.

## Běžné příklady
- Instalace balíčku:
  ```bash
  pkg install název_balíčku
  ```

- Odstranění balíčku:
  ```bash
  pkg remove název_balíčku
  ```

- Aktualizace seznamu balíčků:
  ```bash
  pkg update
  ```

- Aktualizace všech nainstalovaných balíčků:
  ```bash
  pkg upgrade
  ```

- Hledání balíčku podle názvu:
  ```bash
  pkg search klíčové_slovo
  ```

## Tipy
- Před instalací nového balíčku vždy proveďte `pkg update`, abyste měli aktuální seznam dostupných verzí.
- Používejte `pkg search`, abyste se ujistili, že balíček, který chcete nainstalovat, je dostupný.
- Při odstraňování balíčků buďte opatrní, abyste neodstranili závislosti, které by mohly ovlivnit funkčnost jiných aplikací.