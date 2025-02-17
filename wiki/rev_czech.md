# [Linux] Bash rev: obrátí znaky v řetězci

## Přehled
Příkaz `rev` v Bashu slouží k obrácení znaků v každém řádku vstupního textu. To znamená, že pokud máte textový soubor nebo vstup, `rev` přehodí pořadí znaků v každém řádku, což může být užitečné pro různé textové manipulace.

## Použití
Základní syntaxe příkazu `rev` je následující:

```bash
rev [možnosti] [argumenty]
```

## Běžné možnosti
- `-` : Pokud není uveden žádný argument, `rev` čte ze standardního vstupu.
- `--help` : Zobrazí nápovědu k příkazu `rev`.
- `--version` : Zobrazí informace o verzi příkazu `rev`.

## Běžné příklady
1. **Obrácení textu z příkazového řádku:**

```bash
echo "Ahoj světe" | rev
```
Tento příkaz vrátí: `etěvs johA`

2. **Obrácení obsahu souboru:**

```bash
rev soubor.txt
```
Tento příkaz obrátí znaky v každém řádku souboru `soubor.txt`.

3. **Uložení obráceného textu do nového souboru:**

```bash
rev soubor.txt > obraceny_soubor.txt
```
Tento příkaz uloží obrácený text do souboru `obraceny_soubor.txt`.

4. **Obrácení více řádků z textového souboru:**

```bash
cat soubor.txt | rev
```
Tento příkaz použije `cat` k zobrazení obsahu souboru a poté obrátí znaky každého řádku.

## Tipy
- Pokud chcete obrátit pouze část textu, můžete použít příkaz `head` nebo `tail` v kombinaci s `rev`.
- Příkaz `rev` je skvělý pro rychlé testování a manipulaci s textem, ale pro složitější úkoly zvažte použití skriptování v Bash.
- Mějte na paměti, že `rev` neprovádí žádné změny v původním souboru, pokud explicitně neukládáte výstup do nového souboru.