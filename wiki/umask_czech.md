# [Linux] Bash umask použití: Nastavení výchozího oprávnění souborů

## Přehled
Příkaz `umask` slouží k nastavení výchozích oprávnění pro nové soubory a adresáře v systému. Oprávnění určuje, kdo může soubory číst, zapisovat nebo je spouštět. Umask definuje, které oprávnění budou odečteny od výchozích hodnot při vytváření nových souborů a adresářů.

## Použití
Základní syntaxe příkazu `umask` je následující:

```bash
umask [možnosti] [argumenty]
```

## Běžné možnosti
- `-S`: Zobrazí umask v symbolickém formátu.
- `-p`: Zobrazí aktuální umask s podrobnostmi o uživatelském prostředí.

## Běžné příklady
1. **Zobrazení aktuální umask**:
   ```bash
   umask
   ```

2. **Nastavení umask na 022** (nové soubory budou mít oprávnění 644 a nové adresáře 755):
   ```bash
   umask 022
   ```

3. **Nastavení umask na 007** (nové soubory a adresáře budou mít oprávnění 770):
   ```bash
   umask 007
   ```

4. **Zobrazení umask v symbolickém formátu**:
   ```bash
   umask -S
   ```

## Tipy
- Ujistěte se, že umask je nastaven na hodnotu, která odpovídá vašim bezpečnostním požadavkům.
- Při práci v sdílených prostředích může být užitečné nastavit umask tak, aby ostatní uživatelé měli přístup k souborům, které vytváříte.
- Pokud potřebujete dočasně změnit umask, můžete to provést v rámci skriptu nebo terminálové relace a po jejím ukončení se vrátí k původnímu nastavení.