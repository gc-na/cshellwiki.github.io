# [Linux] Bash passwd használat: Jelszókezelés

## Áttekintés
A `passwd` parancs a felhasználói jelszavak kezelésére szolgál a Linux rendszerekben. Ezzel a paranccsal a felhasználók megváltoztathatják a saját jelszavukat, míg a rendszergazdák más felhasználók jelszavát is módosíthatják.

## Használat
A parancs alapvető szintaxisa a következő:

```bash
passwd [opciók] [felhasználónév]
```

## Gyakori opciók
- `-d`: Törli a felhasználó jelszavát.
- `-e`: Azonnali jelszóváltoztatásra kényszeríti a felhasználót.
- `-l`: Lezárja a felhasználói fiókot (jelszó letiltása).
- `-u`: Feloldja a felhasználói fiók zárolását.

## Gyakori példák
1. **Saját jelszó megváltoztatása:**
   ```bash
   passwd
   ```

2. **Más felhasználó jelszavának megváltoztatása (rendszergazda jogokkal):**
   ```bash
   sudo passwd felhasználónév
   ```

3. **Felhasználói fiók lezárása:**
   ```bash
   sudo passwd -l felhasználónév
   ```

4. **Felhasználói jelszó törlése:**
   ```bash
   sudo passwd -d felhasználónév
   ```

## Tippek
- Mindig használj erős jelszót, amely tartalmaz kis- és nagybetűket, számokat és speciális karaktereket.
- Rendszergazdaként légy óvatos a jelszavak módosításakor, hogy ne zárj ki felhasználókat a rendszerből.
- Használj jelszókezelő programokat a jelszavak biztonságos tárolására és kezelésére.