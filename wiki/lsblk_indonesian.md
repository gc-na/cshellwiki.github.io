# [Linux] C Shell (csh) lsblk Penggunaan: Menampilkan informasi tentang perangkat blok

## Overview
Perintah `lsblk` digunakan untuk menampilkan informasi tentang perangkat blok di sistem Linux. Ini termasuk disk, partisi, dan perangkat penyimpanan lainnya, memberikan gambaran yang jelas tentang struktur penyimpanan di sistem Anda.

## Usage
Berikut adalah sintaks dasar dari perintah `lsblk`:

```csh
lsblk [options] [arguments]
```

## Common Options
- `-a` : Menampilkan semua perangkat, termasuk yang tidak terpasang.
- `-f` : Menampilkan informasi sistem file pada perangkat.
- `-l` : Menampilkan output dalam format daftar (list).
- `-o` : Menentukan kolom yang ingin ditampilkan.
- `-p` : Menampilkan nama perangkat lengkap.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `lsblk`:

1. Menampilkan semua perangkat blok:
   ```csh
   lsblk
   ```

2. Menampilkan semua perangkat termasuk yang tidak terpasang:
   ```csh
   lsblk -a
   ```

3. Menampilkan informasi sistem file:
   ```csh
   lsblk -f
   ```

4. Menampilkan output dalam format daftar:
   ```csh
   lsblk -l
   ```

5. Menentukan kolom yang ingin ditampilkan:
   ```csh
   lsblk -o NAME,SIZE,TYPE,MOUNTPOINT
   ```

## Tips
- Gunakan opsi `-f` untuk mendapatkan informasi lebih detail tentang sistem file pada perangkat.
- Kombinasikan opsi untuk menyesuaikan output sesuai kebutuhan Anda, misalnya `lsblk -a -f`.
- Selalu periksa perangkat yang terpasang sebelum melakukan operasi yang dapat mempengaruhi data, seperti format atau penghapusan.