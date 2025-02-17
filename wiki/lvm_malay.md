# [Linux] Bash lvm Penggunaan: Mengurus Logical Volume Management

## Overview
Perintah `lvm` digunakan untuk mengurus Logical Volume Management (LVM) dalam sistem Linux. LVM membolehkan pengguna untuk mengurus ruang penyimpanan dengan lebih fleksibel, termasuk mencipta, mengubah saiz, dan memadam volume logik.

## Usage
Berikut adalah sintaks asas untuk perintah `lvm`:

```bash
lvm [options] [arguments]
```

## Common Options
- `create`: Mencipta volume logik baru.
- `remove`: Memadam volume logik.
- `extend`: Mengubah saiz volume logik dengan menambah ruang.
- `reduce`: Mengubah saiz volume logik dengan mengurangkan ruang.
- `lvdisplay`: Menunjukkan maklumat tentang volume logik yang ada.

## Common Examples
Berikut adalah beberapa contoh penggunaan `lvm`:

### Mencipta Volume Logik
```bash
lvcreate -n myvolume -L 10G myvg
```
Perintah ini mencipta volume logik bernama `myvolume` dengan saiz 10GB dalam kumpulan volum `myvg`.

### Memadam Volume Logik
```bash
lvremove /dev/myvg/myvolume
```
Perintah ini memadam volume logik `myvolume` dari kumpulan volum `myvg`.

### Mengubah Saiz Volume Logik
#### Menambah Ruang
```bash
lvextend -L +5G /dev/myvg/myvolume
```
Perintah ini menambah 5GB kepada volume logik `myvolume`.

#### Mengurangkan Ruang
```bash
lvreduce -L -5G /dev/myvg/myvolume
```
Perintah ini mengurangkan 5GB dari volume logik `myvolume`.

### Menunjukkan Maklumat Volume Logik
```bash
lvdisplay
```
Perintah ini menunjukkan maklumat terperinci tentang semua volume logik yang ada.

## Tips
- Sentiasa buat salinan data penting sebelum melakukan pengubahsuaian pada volume logik.
- Gunakan perintah `lvdisplay` untuk memeriksa keadaan volume logik sebelum dan selepas melakukan perubahan.
- Pastikan untuk memeriksa ruang yang tersedia dalam kumpulan volum sebelum menambah atau mengurangkan saiz volume logik.