# [Linux] Bash mount használata: Fájl- és könyvtárak csatlakoztatása

## Áttekintés
A `mount` parancs lehetővé teszi a fájl- és könyvtárak csatlakoztatását a fájlrendszerhez. Ezzel a paranccsal különböző tárolóeszközöket, például USB-meghajtókat vagy hálózati megosztásokat csatlakoztathatunk a rendszerhez, így azok elérhetővé válnak a fájlrendszerben.

## Használat
A `mount` parancs alapvető szintaxisa a következő:

```bash
mount [opciók] [argumentumok]
```

## Gyakori opciók
- `-t <típus>`: Megadja a fájlrendszer típusát (pl. ext4, ntfs).
- `-o <opciók>`: Speciális opciók megadása, mint például `ro` (csak olvasható) vagy `rw` (olvasható-írható).
- `-a`: Minden fájlrendszert csatlakoztat, amelyet a `/etc/fstab` fájlban definiáltak.
- `-r`: Csak olvasható módban csatlakoztatja a fájlrendszert.

## Gyakori példák
1. **USB-meghajtó csatlakoztatása**:
   ```bash
   mount /dev/sdb1 /mnt/usb
   ```
   Ez a parancs a `/dev/sdb1` USB-meghajtót csatlakoztatja a `/mnt/usb` könyvtárhoz.

2. **Hálózati megosztás csatlakoztatása**:
   ```bash
   mount -t nfs 192.168.1.100:/shared /mnt/nfs
   ```
   Ezzel a paranccsal egy NFS megosztást csatlakoztatunk a helyi `/mnt/nfs` könyvtárhoz.

3. **Csak olvasható módban történő csatlakoztatás**:
   ```bash
   mount -o ro /dev/sdc1 /mnt/read_only
   ```
   Ez a parancs a `/dev/sdc1` meghajtót csak olvasható módban csatlakoztatja.

## Tippek
- Mindig ellenőrizd, hogy a csatlakoztatni kívánt eszköz nem használatban van-e, hogy elkerüld az adatvesztést.
- Használj `umount` parancsot a csatlakoztatott fájlrendszer leválasztásához, mielőtt fizikailag eltávolítanád az eszközt.
- A `/etc/fstab` fájlban előre definiálhatod a fájlrendszereket, így a rendszer indításakor automatikusan csatlakoztatásra kerülnek.