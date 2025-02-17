# [Linux] Bash fmt použití: Formátování textových souborů

## Přehled
Příkaz `fmt` slouží k formátování textových souborů. Jeho hlavním cílem je upravit text tak, aby byl lépe čitelný, a to zejména tím, že se automaticky přizpůsobí šířce výstupu. Tento příkaz je užitečný pro úpravu textu, který je příliš široký nebo má nepravidelné řádky.

## Použití
Základní syntaxe příkazu `fmt` je následující:

```bash
fmt [možnosti] [argumenty]
```

## Běžné možnosti
- `-w, --width=N` - nastaví maximální šířku řádku na N znaků.
- `-s, --split-only` - rozdělí pouze dlouhé řádky, aniž by prováděl další úpravy.
- `-u, --uniform` - zajišťuje, že všechny řádky mají stejnou délku.

## Běžné příklady
1. Základní použití pro formátování souboru `text.txt`:
   ```bash
   fmt text.txt
   ```

2. Nastavení maximální šířky řádku na 50 znaků:
   ```bash
   fmt -w 50 text.txt
   ```

3. Použití s volbou `-s` pro rozdělení pouze dlouhých řádků:
   ```bash
   fmt -s text.txt
   ```

4. Formátování textu z příkazového řádku:
   ```bash
   echo "Toto je velmi dlouhý text, který potřebuje být formátován." | fmt -w 40
   ```

## Tipy
- Při práci s dlouhými textovými soubory je dobré experimentovat s různými hodnotami šířky, abyste našli optimální nastavení pro čitelnost.
- Pokud potřebujete zachovat určité mezery v textu, použijte volbu `-s`, aby se zabránilo nežádoucím úpravám.
- Pro skripty a automatizaci můžete kombinovat `fmt` s dalšími příkazy, jako je `cat` nebo `grep`, pro efektivnější zpracování textu.