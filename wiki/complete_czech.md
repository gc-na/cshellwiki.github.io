# [Linux] Bash complete použití: Automatické doplňování příkazů

## Přehled
Příkaz `complete` v Bash slouží k definování a přizpůsobení automatického doplňování příkazů. Umožňuje uživatelům specifikovat, jaké argumenty nebo volby by měly být navrženy při používání tabulátoru pro doplnění příkazů.

## Použití
Základní syntaxe příkazu `complete` je následující:

```bash
complete [options] [arguments]
```

## Běžné možnosti
- `-o`: Určuje volby pro doplňování, jako například `default`, `nospace`, nebo `filenames`.
- `-F`: Umožňuje specifikovat funkci, která generuje návrhy pro doplňování.
- `-A`: Definuje typ argumentu, například `command`, `file`, nebo `directory`.

## Běžné příklady
1. **Základní použití pro příkaz `mycmd`:**
   ```bash
   complete mycmd
   ```

2. **Doplňování souborů pro příkaz `mycmd`:**
   ```bash
   complete -f mycmd
   ```

3. **Použití funkce pro generování návrhů:**
   ```bash
   _mycmd_completions() {
       COMPREPLY=( $(compgen -W "option1 option2 option3" -- "${COMP_WORDS[1]}") )
   }
   complete -F _mycmd_completions mycmd
   ```

4. **Doplňování pro příkaz s volbami:**
   ```bash
   complete -o nospace mycmd
   ```

## Tipy
- Vždy testujte nové nastavení doplňování v interaktivním shellu, abyste se ujistili, že funguje podle očekávání.
- Používejte funkce pro složitější logiku doplňování, což vám umožní přizpůsobit chování podle kontextu.
- Zvažte přidání dokumentace k vlastním příkazům, aby ostatní uživatelé věděli, jaké možnosti doplňování jsou k dispozici.