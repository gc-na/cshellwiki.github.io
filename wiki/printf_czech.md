# [Linux] Bash printf použití: Formátování a výstup textu

## Přehled
Příkaz `printf` v Bash slouží k formátovanému výstupu textu. Umožňuje uživatelům vytvářet strukturované a stylizované výstupy, což je užitečné při zobrazování dat v konzoli.

## Použití
Základní syntaxe příkazu `printf` je následující:

```bash
printf [možnosti] [argumenty]
```

## Běžné možnosti
- `-v` : Uloží výstup do proměnné.
- `-f` : Používá formátovací řetězec.
- `-n` : Nezahrnuje nový řádek na konci výstupu.

## Běžné příklady
1. **Jednoduchý textový výstup:**
   ```bash
   printf "Ahoj, světe!\n"
   ```

2. **Formátování čísel:**
   ```bash
   printf "Číslo: %d\n" 42
   ```

3. **Zarovnání textu:**
   ```bash
   printf "|%-10s|%10s|\n" "Levý" "Pravý"
   ```

4. **Výstup s více formáty:**
   ```bash
   printf "Jméno: %s, Věk: %d\n" "Jan" 30
   ```

5. **Uložení výstupu do proměnné:**
   ```bash
   printf -v result "Výsledek: %.2f" 3.14159
   echo "$result"
   ```

## Tipy
- Vždy používejte formátovací řetězce pro přesné řízení výstupu.
- Nezapomeňte na únikové sekvence, jako je `\n` pro nový řádek nebo `\t` pro tabulátor.
- Testujte příkazy v interaktivním shellu, abyste se ujistili, že výstup odpovídá vašim očekáváním.