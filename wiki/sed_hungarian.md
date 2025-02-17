# [Linux] Bash sed használat: Szövegfeldolgozás és átalakítás

## Áttekintés
A `sed` (stream editor) egy hatékony parancs a szövegfeldolgozásra, amely lehetővé teszi a fájlokban vagy a standard bemeneten található szöveg módosítását. A `sed` segítségével egyszerű keresési és helyettesítési műveleteket végezhetünk, valamint komplex szövegmanipulációkat is végrehajthatunk.

## Használat
A `sed` parancs alapvető szintaxisa a következő:

```bash
sed [opciók] [argumentumok]
```

## Gyakori opciók
- `-e`: Több `sed` parancs megadása egyetlen hívásban.
- `-i`: A fájlok közvetlen módosítása (in-place).
- `-n`: Csak a megadott kimeneteket jeleníti meg, alapértelmezés szerint nem ír ki semmit.
- `s`: Keresés és helyettesítés parancs.

## Gyakori példák

### 1. Egyszerű helyettesítés
A következő példa a "hello" szót "hi"-ra cseréli a bemeneti szövegben.

```bash
echo "hello world" | sed 's/hello/hi/'
```

### 2. Fájlban történő helyettesítés
A `-i` opcióval közvetlenül módosíthatjuk a fájlt.

```bash
sed -i 's/old/new/g' file.txt
```

### 3. Sorok törlése
A következő példa eltávolítja a 2. sort a bemeneti szövegből.

```bash
sed '2d' file.txt
```

### 4. Több parancs végrehajtása
Több `sed` parancsot is végrehajthatunk egy hívásban.

```bash
sed -e 's/foo/bar/' -e 's/baz/qux/' file.txt
```

### 5. Csak a megadott sorok megjelenítése
A `-n` opcióval csak a 1. és 3. sorokat jelenítjük meg.

```bash
sed -n '1p;3p' file.txt
```

## Tippek
- Mindig készítsünk biztonsági másolatot a fájlokról, mielőtt az `-i` opciót használjuk.
- Használjunk reguláris kifejezéseket a `sed` parancsokban a bonyolultabb minták kezelésére.
- Teszteljük a parancsokat a `echo` vagy `cat` parancsokkal, mielőtt fájlokon alkalmaznánk őket, hogy elkerüljük a nem kívánt módosításokat.