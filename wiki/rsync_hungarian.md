# [Linux] Bash rsync használata: Fájlok és könyvtárak szinkronizálása

## Áttekintés
Az `rsync` parancs egy hatékony eszköz fájlok és könyvtárak szinkronizálására helyi és távoli rendszerek között. Képes csak a módosított fájlokat átkonvertálni, így csökkenti az átvitel idejét és sávszélességét.

## Használat
Az `rsync` parancs alapvető szintaxisa a következő:

```bash
rsync [opciók] [forrás] [cél]
```

## Gyakori opciók
- `-a`: Archiválási mód, amely megőrzi a fájlok tulajdonságait.
- `-v`: Verbose, azaz részletes kimenetet ad.
- `-z`: Tömöríti az adatokat az átvitel során.
- `-r`: Rekurzív másolás könyvtárak esetén.
- `--delete`: Törli a cél helyen azokat a fájlokat, amelyek a forrásban már nem találhatók.

## Gyakori példák
1. **Helyi könyvtár szinkronizálása**:
   ```bash
   rsync -av /forras/konyvtar/ /cel/konyvtar/
   ```

2. **Fájlok átvitele távoli szerverre**:
   ```bash
   rsync -av /forras/fajl.txt felhasznalo@tavoli-szerver:/cel/konyvtar/
   ```

3. **Könyvtárak szinkronizálása távoli szerverről**:
   ```bash
   rsync -av felhasznalo@tavoli-szerver:/forras/konyvtar/ /cel/konyvtar/
   ```

4. **Tömörített átvitel**:
   ```bash
   rsync -avz /forras/konyvtar/ felhasznalo@tavoli-szerver:/cel/konyvtar/
   ```

5. **Fájlok törlése a cél helyen**:
   ```bash
   rsync -av --delete /forras/konyvtar/ /cel/konyvtar/
   ```

## Tippek
- Mindig használj `-n` (dry run) opciót, hogy először megnézd, mit fog csinálni az `rsync`, mielőtt végrehajtanád a parancsot.
- Használj SSH-t a távoli átvitelhez a biztonság érdekében, például `rsync -av -e ssh`.
- Rendszeresen készíts biztonsági másolatot fontos fájljaidról az `rsync` segítségével, hogy elkerüld az adatvesztést.