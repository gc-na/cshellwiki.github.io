# [Linux] Bash fold použití: Zalamování textu na pevné šířce

## Přehled
Příkaz `fold` se používá k zalamování textu na pevně stanovenou šířku. Je užitečný při práci s textovými soubory, kde je potřeba zajistit, aby řádky nebyly delší než určité množství znaků, což usnadňuje čtení a zobrazení textu.

## Použití
Základní syntaxe příkazu `fold` je následující:

```
fold [možnosti] [argumenty]
```

## Běžné možnosti
- `-w, --width=N` : Nastaví maximální šířku řádku na N znaků.
- `-s, --spaces` : Zalamuje text na posledním mezerovém znaku před dosažením maximální šířky.
- `-b, --bytes` : Místo znaků používá pro šířku bajty.

## Běžné příklady
Zde je několik praktických příkladů použití příkazu `fold`:

1. **Zalamování textového souboru na 50 znaků:**
   ```bash
   fold -w 50 soubor.txt
   ```

2. **Zalamování textu s mezerami:**
   ```bash
   fold -s -w 30 soubor.txt
   ```

3. **Zalamování textu a výstup do nového souboru:**
   ```bash
   fold -w 60 soubor.txt > zalomeny_soubor.txt
   ```

4. **Zalamování textu v příkazovém řádku:**
   ```bash
   echo "Toto je dlouhý text, který chceme zalomit." | fold -w 20
   ```

## Tipy
- Při práci s textovými soubory se ujistěte, že máte zálohu, pokud provádíte změny.
- Používejte možnost `-s`, pokud chcete, aby text byl zalamován na slovech, což zlepší čitelnost.
- Experimentujte s různými šířkami, abyste našli optimální nastavení pro vaše potřeby.