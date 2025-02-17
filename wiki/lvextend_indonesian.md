# [Linux] Bash lvextend Penggunaan: Memperbesar ukuran Logical Volume

## Overview
Perintah `lvextend` digunakan untuk memperbesar ukuran Logical Volume (LV) dalam sistem manajemen volume logis (LVM). Dengan menggunakan perintah ini, Anda dapat menambah ruang penyimpanan pada volume yang sudah ada, memungkinkan Anda untuk mengelola ruang disk dengan lebih efisien.

## Usage
Berikut adalah sintaks dasar dari perintah `lvextend`:

```
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: Menambah ukuran LV dengan ukuran yang ditentukan. Misalnya, `-L +10G` untuk menambah 10 GB.
- `-l +size`: Menambah ukuran LV dengan jumlah logical extents yang ditentukan.
- `-r`: Secara otomatis memperluas filesystem setelah LV diperbesar.
- `-n`: Mengubah nama Logical Volume.

## Common Examples
Berikut adalah beberapa contoh penggunaan `lvextend`:

1. **Menambah 10 GB pada Logical Volume**:
   ```bash
   lvextend -L +10G /dev/vg01/lv01
   ```

2. **Menambah ukuran LV dengan logical extents**:
   ```bash
   lvextend -l +100 /dev/vg01/lv01
   ```

3. **Menambah ukuran LV dan memperluas filesystem secara otomatis**:
   ```bash
   lvextend -r -L +5G /dev/vg01/lv01
   ```

4. **Mengubah nama Logical Volume**:
   ```bash
   lvextend -n new_lv_name /dev/vg01/old_lv_name
   ```

## Tips
- Selalu pastikan untuk memeriksa ruang yang tersedia pada Volume Group (VG) sebelum memperbesar LV.
- Gunakan opsi `-r` jika Anda ingin memperluas filesystem secara otomatis setelah memperbesar LV, untuk menghindari langkah tambahan.
- Lakukan backup data penting sebelum melakukan perubahan pada Logical Volume untuk menghindari kehilangan data.