# [Linux] Bash expand használat: Szöveg tabulátorokkal való kiegészítése

## Áttekintés
Az `expand` parancs a szöveges fájlokban található tabulátorokat (TAB) szóközökre cseréli, lehetővé téve a szöveg formázását és olvashatóságának javítását.

## Használat
A `expand` parancs alapvető szintaxisa a következő:

```bash
expand [opciók] [argumentumok]
```

## Gyakori Opciók
- `-t, --tabs=N`: Beállítja a tabulátorok helyettesítésének méretét N számú szóközre.
- `-i, --initial`: Csak a szöveg elején található tabulátorokat cseréli.
- `-n, --no-tabs`: Nem cseréli le a tabulátorokat, csak a szóközöket hagyja érintetlenül.

## Gyakori Példák
1. **Alapvető használat**: Tabulátorok cseréje szóközökre a `file.txt` fájlban.
   ```bash
   expand file.txt
   ```

2. **Tabulátorok méretének beállítása**: Tabulátorok cseréje 4 szóközre.
   ```bash
   expand -t 4 file.txt
   ```

3. **Csak az elején található tabulátorok cseréje**: Tabulátorok cseréje csak a szöveg elején.
   ```bash
   expand -i file.txt
   ```

4. **Tabulátorok cseréje egy új fájlba**: Az `output.txt` fájlba menti a módosított szöveget.
   ```bash
   expand file.txt > output.txt
   ```

## Tippek
- Használja az `-t` opciót, ha a tabulátorok méretét a projekt igényeihez szeretné igazítani.
- Ellenőrizze a fájl formázását a `cat -A` paranccsal, hogy lássa, hol találhatók a tabulátorok.
- A `expand` parancsot gyakran használják a szöveges fájlok előkészítésére, mielőtt más programokkal dolgoznának, mint például a `pr` vagy a `fmt`.