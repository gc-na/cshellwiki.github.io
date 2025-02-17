# [Linux] Bash chmod použití: Nastavení oprávnění souborů

## Přehled
Příkaz `chmod` slouží k nastavení oprávnění k souborům a adresářům v systému Linux. Umožňuje uživatelům řídit, kdo může soubory číst, zapisovat nebo je spouštět.

## Použití
Základní syntaxe příkazu `chmod` je následující:

```bash
chmod [možnosti] [argumenty]
```

## Běžné možnosti
- `-R`: Rekurzivně mění oprávnění pro všechny soubory a adresáře v daném umístění.
- `u`: Oprávnění pro vlastníka souboru.
- `g`: Oprávnění pro skupinu.
- `o`: Oprávnění pro ostatní uživatele.
- `a`: Oprávnění pro všechny uživatele (vlastník, skupina, ostatní).
- `+`: Přidává oprávnění.
- `-`: Odebere oprávnění.
- `=`: Nastaví oprávnění na specifikované hodnoty.

## Běžné příklady
1. **Nastavení oprávnění pro vlastníka na čtení a zápis:**
   ```bash
   chmod u+rw soubor.txt
   ```

2. **Odebrání oprávnění pro skupinu:**
   ```bash
   chmod g-r soubor.txt
   ```

3. **Nastavení oprávnění pro všechny uživatele na čtení:**
   ```bash
   chmod a+r soubor.txt
   ```

4. **Rekurzivní změna oprávnění pro adresář:**
   ```bash
   chmod -R 755 adresar/
   ```

5. **Nastavení oprávnění na spouštění pro vlastníka:**
   ```bash
   chmod u+x skript.sh
   ```

## Tipy
- Před provedením změn oprávnění si vždy zkontrolujte aktuální nastavení pomocí příkazu `ls -l`.
- Používejte rekurzivní možnost `-R` opatrně, abyste nezměnili oprávnění pro soubory, které by měly zůstat chráněné.
- Pokud si nejste jisti, jaká oprávnění použít, začněte s méně přístupnými možnostmi a postupně je rozšiřujte podle potřeby.