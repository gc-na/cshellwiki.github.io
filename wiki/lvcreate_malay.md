# [Linux] Bash lvcreate Penggunaan: Membuat Logical Volume

## Overview
Perintah `lvcreate` digunakan dalam sistem pengurusan storan Linux untuk membuat logical volume (LV) dalam volume group (VG). Logical volume ini membolehkan pengguna untuk menguruskan ruang storan dengan lebih fleksibel dan berkesan.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `lvcreate`:

```bash
lvcreate [options] [arguments]
```

## Common Options
Beberapa pilihan biasa untuk `lvcreate` termasuk:

- `-n, --name <name>`: Menetapkan nama untuk logical volume yang akan dibuat.
- `-L, --size <size>`: Menentukan saiz logical volume.
- `-l, --extents <number>`: Menentukan jumlah extents yang akan digunakan untuk logical volume.
- `-m, --mirrors <number>`: Menentukan bilangan salinan (mirror) untuk logical volume.
- `-Z, --zero n`: Menentukan sama ada untuk mengisi logical volume dengan sifar.

## Common Examples
Berikut adalah beberapa contoh praktikal penggunaan `lvcreate`:

1. **Membuat Logical Volume dengan Nama dan Saiz**
   ```bash
   lvcreate -n my_volume -L 10G my_volume_group
   ```

2. **Membuat Logical Volume dengan Jumlah Extents**
   ```bash
   lvcreate -l 100 -n my_extent_volume my_volume_group
   ```

3. **Membuat Logical Volume dengan Mirror**
   ```bash
   lvcreate -m 1 -n my_mirror_volume -L 5G my_volume_group
   ```

4. **Membuat Logical Volume dan Mengisi dengan Sifar**
   ```bash
   lvcreate -n my_zeroed_volume -L 20G -Z y my_volume_group
   ```

## Tips
- Pastikan anda mempunyai cukup ruang dalam volume group sebelum mencipta logical volume.
- Gunakan nama yang jelas dan deskriptif untuk logical volume anda untuk memudahkan pengurusan.
- Periksa status logical volume selepas penciptaan dengan menggunakan perintah `lvdisplay` untuk memastikan ia telah dibuat dengan betul.