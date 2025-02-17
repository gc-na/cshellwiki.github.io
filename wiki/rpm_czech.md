# [Linux] Bash rpm použití: Správa balíčků RPM

## Přehled
Příkaz `rpm` se používá pro správu balíčků v systému Linux, který používá formát RPM (Red Hat Package Manager). Umožňuje instalaci, odinstalaci, aktualizaci a kontrolu balíčků.

## Použití
Základní syntaxe příkazu `rpm` je následující:

```bash
rpm [options] [arguments]
```

## Běžné možnosti
- `-i`: Instalace nového balíčku.
- `-e`: Odinstalace balíčku.
- `-U`: Aktualizace balíčku na novější verzi.
- `-q`: Dotaz na informace o nainstalovaných balíčcích.
- `--info`: Zobrazení podrobných informací o balíčku.
- `--verify`: Ověření integrity nainstalovaného balíčku.

## Běžné příklady
### Instalace balíčku
Chcete-li nainstalovat balíček, použijte:

```bash
rpm -i balicek.rpm
```

### Odinstalace balíčku
Pro odinstalaci balíčku použijte:

```bash
rpm -e nazev_balicku
```

### Aktualizace balíčku
Pro aktualizaci balíčku na novější verzi použijte:

```bash
rpm -U balicek.nova_verze.rpm
```

### Dotaz na nainstalované balíčky
Chcete-li zjistit, zda je balíček nainstalován, použijte:

```bash
rpm -q nazev_balicku
```

### Zobrazení informací o balíčku
Pro zobrazení podrobných informací o balíčku použijte:

```bash
rpm --info balicek.rpm
```

## Tipy
- Před instalací nového balíčku se ujistěte, že máte všechny potřebné závislosti.
- Používejte `rpm -q` pro kontrolu, zda je balíček již nainstalován, abyste se vyhnuli chybám při instalaci.
- Při odinstalaci balíčku buďte opatrní, abyste neodstranili balíčky, které jsou závislé na jiných aplikacích.