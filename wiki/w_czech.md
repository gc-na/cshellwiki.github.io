# [Linux] Bash w použití: Zobrazí aktivní uživatele a jejich činnost

## Přehled
Příkaz `w` v systému Linux slouží k zobrazení seznamu aktuálně přihlášených uživatelů a jejich aktivit. Tento příkaz poskytuje informace o tom, kdo je přihlášen, jak dlouho jsou přihlášeni, a co právě dělají.

## Použití
Základní syntaxe příkazu `w` je následující:

```bash
w [možnosti] [argumenty]
```

## Běžné možnosti
- `-h`: Skryje hlavičku výstupu.
- `-s`: Zobrazí zjednodušenou verzi výstupu.
- `-u`: Zobrazí uživatelské jméno včetně informací o aktivitě.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `w`:

1. Základní použití pro zobrazení aktuálních uživatelů:
   ```bash
   w
   ```

2. Zobrazení výstupu bez hlavičky:
   ```bash
   w -h
   ```

3. Zjednodušená verze výstupu:
   ```bash
   w -s
   ```

4. Zobrazení uživatelského jména a aktivit:
   ```bash
   w -u
   ```

## Tipy
- Používejte příkaz `w` pravidelně pro sledování aktivit uživatelů na serveru.
- Kombinujte `w` s dalšími příkazy, jako je `grep`, pro filtrování specifických uživatelů.
- Mějte na paměti, že příkaz `w` může vyžadovat administrátorská práva pro zobrazení všech uživatelů na systému.