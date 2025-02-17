# [Linux] Bash lvextend: Memperluas saiz logical volume

## Overview
Perintah `lvextend` digunakan untuk memperbesar saiz logical volume dalam sistem pengurusan volume logik (LVM) pada Linux. Dengan menggunakan perintah ini, anda boleh menambah ruang pada volume yang sedia ada tanpa kehilangan data.

## Usage
Berikut adalah sintaks asas untuk menggunakan `lvextend`:

```bash
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: Menambah saiz tertentu kepada logical volume.
- `-l +number_of_extents`: Menambah bilangan extents kepada logical volume.
- `-r`: Secara automatik mengubah saiz sistem fail yang berkaitan dengan logical volume selepas ia diperbesar.
- `-n new_name`: Menukar nama logical volume semasa.

## Common Examples
1. **Menambah 10GB kepada logical volume:**
   ```bash
   lvextend -L +10G /dev/vg_name/lv_name
   ```

2. **Menambah ruang berdasarkan extents:**
   ```bash
   lvextend -l +100 /dev/vg_name/lv_name
   ```

3. **Memperbesar logical volume dan secara automatik mengubah saiz sistem fail:**
   ```bash
   lvextend -r -L +5G /dev/vg_name/lv_name
   ```

4. **Menukar nama logical volume:**
   ```bash
   lvextend -n new_lv_name /dev/vg_name/lv_name
   ```

## Tips
- Sentiasa pastikan anda mempunyai sandaran data sebelum melakukan perubahan pada logical volume.
- Gunakan pilihan `-r` untuk mengubah saiz sistem fail secara automatik, tetapi pastikan sistem fail yang digunakan menyokong pengubahsuaian saiz secara langsung.
- Periksa ruang yang tersedia dalam volume group sebelum memperbesar logical volume untuk mengelakkan masalah kekurangan ruang.