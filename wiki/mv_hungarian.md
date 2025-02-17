# [Linux] Bash mv használata: Fájlok és könyvtárak áthelyezése vagy átnevezése

## Áttekintés
A `mv` parancs a Bash környezetben fájlok és könyvtárak áthelyezésére vagy átnevezésére szolgál. Ezzel a paranccsal könnyedén módosíthatjuk a fájlok helyét vagy nevét a fájlrendszerben.

## Használat
A `mv` parancs alapvető szintaxisa a következő:

```bash
mv [opciók] [forrás] [cél]
```

## Gyakori opciók
- `-i`: Kérdezzen rá, mielőtt felülírna egy meglévő fájlt.
- `-u`: Csak akkor mozgassa a fájlt, ha a forrás újabb, mint a célfájl, vagy ha a célfájl nem létezik.
- `-v`: Részletes kimenetet ad, megmutatva, hogy mely fájlokat mozgattunk.

## Gyakori példák
1. Fájl áthelyezése egy másik könyvtárba:
   ```bash
   mv myfile.txt /home/user/documents/
   ```

2. Fájl átnevezése:
   ```bash
   mv oldname.txt newname.txt
   ```

3. Több fájl áthelyezése egy könyvtárba:
   ```bash
   mv file1.txt file2.txt /home/user/documents/
   ```

4. Fájl áthelyezése, ha a célfájl már létezik (interaktív mód):
   ```bash
   mv -i myfile.txt /home/user/documents/
   ```

## Tippek
- Mindig használja az `-i` opciót, ha nem biztos abban, hogy a célfájl létezik, hogy elkerülje a véletlen felülírást.
- Ellenőrizze a fájlok helyét a `ls` paranccsal a `mv` parancs végrehajtása előtt, hogy biztos legyen benne, hogy a megfelelő fájlokat mozgassa.
- Használja a `-v` opciót, ha szeretné látni a parancs végrehajtásának részleteit, különösen, ha több fájlt mozgat egyszerre.