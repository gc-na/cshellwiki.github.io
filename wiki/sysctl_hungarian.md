# [Linux] Bash sysctl használata: Rendszerparaméterek kezelése

## Áttekintés
A `sysctl` parancs lehetővé teszi a Linux kernel paramétereinek megtekintését és módosítását futásidőben. Ezzel a parancsal a rendszergazdák beállíthatják a rendszer teljesítményét és viselkedését anélkül, hogy újra kellene indítaniuk a rendszert.

## Használat
A `sysctl` parancs alapvető szintaxisa a következő:

```bash
sysctl [opciók] [argumentumok]
```

## Gyakori Opciók
- `-a`: Megjeleníti az összes elérhető kernel paramétert és azok értékeit.
- `-w`: Módosít egy kernel paramétert az új értékre.
- `-n`: Csak az értéket jeleníti meg, anélkül, hogy a paraméter nevét kiírná.

## Gyakori Példák
- Az összes kernel paraméter megjelenítése:

```bash
sysctl -a
```

- Egy kernel paraméter értékének megtekintése (pl. `vm.swappiness`):

```bash
sysctl vm.swappiness
```

- A `vm.swappiness` paraméter értékének módosítása 10-re:

```bash
sysctl -w vm.swappiness=10
```

- A módosítások állandóvá tétele a `/etc/sysctl.conf` fájlban:

```bash
echo "vm.swappiness=10" >> /etc/sysctl.conf
sysctl -p
```

## Tippek
- Mindig készítsen biztonsági másolatot a konfigurációs fájlokról, mielőtt módosítaná őket.
- Használja a `sysctl -n` opciót, ha csak az értékre van szüksége, hogy elkerülje a felesleges információt.
- Ellenőrizze a paraméterek hatását a rendszer teljesítményére, mielőtt véglegesen módosítaná őket.