# [Linux] Bash chkconfig használat: Szolgáltatások kezelése indításkor

## Áttekintés
A `chkconfig` parancs a Linux rendszerekben a szolgáltatások indítási szintjeinek kezelésére szolgál. Lehetővé teszi a felhasználók számára, hogy be- és kikapcsolják a szolgáltatásokat a rendszer indításakor, így könnyen testre szabhatják a rendszer indítási folyamatát.

## Használat
A `chkconfig` parancs alapvető szintaxisa a következő:

```bash
chkconfig [opciók] [argumentumok]
```

## Gyakori opciók
- `--list`: Megjeleníti az összes szolgáltatás indítási szintjeit.
- `--add <szolgáltatás>`: Hozzáad egy új szolgáltatást a rendszerhez.
- `--del <szolgáltatás>`: Eltávolít egy szolgáltatást a rendszerből.
- `--level <szint> <szolgáltatás> <on|off>`: Beállítja a megadott szolgáltatás indítási szintjét.

## Gyakori példák
1. Az összes szolgáltatás indítási szintjeinek megjelenítése:
   ```bash
   chkconfig --list
   ```

2. Egy új szolgáltatás hozzáadása:
   ```bash
   chkconfig --add myservice
   ```

3. Egy szolgáltatás eltávolítása:
   ```bash
   chkconfig --del myservice
   ```

4. A `httpd` szolgáltatás engedélyezése a 3-as és 5-ös indítási szinten:
   ```bash
   chkconfig --level 35 httpd on
   ```

5. A `cron` szolgáltatás letiltása az összes indítási szinten:
   ```bash
   chkconfig cron off
   ```

## Tippek
- Mindig ellenőrizd a szolgáltatások állapotát a `chkconfig --list` parancs használatával, mielőtt módosítanád őket.
- Használj `sudo`-t a parancsok előtt, ha rendszergazdai jogosultságokra van szükséged.
- A szolgáltatások indítási szintjeinek megértése segíthet a rendszer teljesítményének optimalizálásában.