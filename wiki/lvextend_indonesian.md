# [Linux] C Shell (csh) lvextend Penggunaan: Memperluas ukuran logical volume

## Overview
Perintah `lvextend` digunakan untuk memperbesar ukuran logical volume dalam sistem manajemen volume logis (LVM). Dengan menggunakan `lvextend`, Anda dapat menambah ruang penyimpanan pada volume yang sudah ada tanpa kehilangan data.

## Usage
Berikut adalah sintaks dasar dari perintah `lvextend`:

```shell
lvextend [options] [arguments]
```

## Common Options
- `-L +size`: Menambah ukuran logical volume dengan ukuran yang ditentukan.
- `-l +number`: Menambah ukuran logical volume dengan jumlah logical extents yang ditentukan.
- `-r`: Secara otomatis memperluas filesystem yang terkait dengan logical volume setelah perpanjangan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `lvextend`:

1. Menambah ukuran logical volume sebesar 10GB:
   ```shell
   lvextend -L +10G /dev/vg01/lv01
   ```

2. Menambah ukuran logical volume dengan jumlah extents:
   ```shell
   lvextend -l +100 /dev/vg01/lv01
   ```

3. Menambah ukuran logical volume dan secara otomatis memperluas filesystem:
   ```shell
   lvextend -r -L +5G /dev/vg01/lv01
   ```

## Tips
- Pastikan untuk memeriksa ruang fisik yang tersedia sebelum memperluas logical volume dengan menggunakan perintah `vgs`.
- Selalu lakukan backup data penting sebelum melakukan perubahan pada volume untuk menghindari kehilangan data.
- Gunakan opsi `-r` jika Anda ingin memperluas filesystem secara otomatis setelah memperbesar logical volume, untuk menghemat waktu dan usaha.