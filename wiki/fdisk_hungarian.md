# [Linux] Bash fdisk használata: Partíciók kezelése

## Áttekintés
Az `fdisk` parancs egy erőteljes eszköz a Linux rendszerekben, amelyet a lemezek partícióinak kezelésére használnak. Lehetővé teszi a felhasználók számára, hogy partíciókat hozzanak létre, töröljenek, módosítsanak és információkat nyerjenek ki a tárolóeszközökről.

## Használat
A `fdisk` parancs alapvető szintaxisa a következő:

```bash
fdisk [opciók] [eszköz]
```

## Gyakori Opciók
- `-l`: Listázza az összes elérhető partíciót a rendszerben.
- `-u`: A méreteket szektorokban adja meg, nem pedig megabájtban.
- `-n`: Új partíció létrehozása.
- `-d`: Partíció törlése.
- `-p`: A partíciók részletes információinak megjelenítése.

## Gyakori Példák

1. **Partíciók listázása**:
   A rendszer összes partíciójának megjelenítése.
   ```bash
   fdisk -l
   ```

2. **Új partíció létrehozása**:
   Egy új partíció létrehozása a `/dev/sda` eszközön.
   ```bash
   fdisk /dev/sda
   ```
   (Ezután kövesse az interaktív utasításokat a partíció létrehozásához.)

3. **Partíció törlése**:
   Egy meglévő partíció törlése a `/dev/sda` eszközön.
   ```bash
   fdisk /dev/sda
   ```
   (Válassza a törlés opciót az interaktív menüben.)

4. **Partíciós táblázat megjelenítése**:
   A partíciós táblázat részletes információinak megjelenítése.
   ```bash
   fdisk -p /dev/sda
   ```

## Tippek
- Mindig készítsen biztonsági másolatot az adatairól, mielőtt partíciókat módosítana.
- Használja a `-l` opciót, hogy gyorsan áttekintse a rendszer összes partícióját.
- Legyen óvatos a partíciók törlésekor, mivel ez adatvesztéshez vezethet.
- Az `fdisk` használata előtt érdemes alaposan megismerkedni a parancs interaktív menüjével.