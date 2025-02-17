# [Linux] Bash resize2fs használata: A fájlrendszer méretének módosítása

## Áttekintés
A `resize2fs` parancs a Linux operációs rendszerben használt eszköz, amely lehetővé teszi a fájlrendszerek méretének módosítását. Ezt a parancsot általában akkor használják, amikor a fájlrendszer méretét a partíció méretének megváltoztatása után kell igazítani.

## Használat
A `resize2fs` parancs alapvető szintaxisa a következő:

```bash
resize2fs [opciók] [argumentumok]
```

## Gyakori opciók
- `-f`: Kényszeríti a fájlrendszer átméretezését, még akkor is, ha a fájlrendszer nem igényli.
- `-p`: Megjeleníti a folyamat előrehaladását.
- `-s`: Csak a fájlrendszer méretének csökkentésére használható.
- `-M`: A fájlrendszer minimális méretre csökkentése.

## Gyakori példák
1. **Fájlrendszer méretének növelése**:
   ```bash
   resize2fs /dev/sda1
   ```

2. **Fájlrendszer méretének csökkentése** (csak ha a fájlrendszer nem használatban van):
   ```bash
   resize2fs -s /dev/sda1 10G
   ```

3. **Folyamat előrehaladásának megjelenítése**:
   ```bash
   resize2fs -p /dev/sda1
   ```

4. **Fájlrendszer minimális méretre csökkentése**:
   ```bash
   resize2fs -M /dev/sda1
   ```

## Tippek
- Mindig készítsen biztonsági másolatot a fontos adatairól, mielőtt átméretezné a fájlrendszert.
- Ellenőrizze a fájlrendszert a `fsck` paranccsal, mielőtt átméretezné.
- Győződjön meg róla, hogy a fájlrendszer nem használatban van az átméretezés előtt, különösen csökkentés esetén.