# [Linux] Bash resize2fs Penggunaan: Mengubah saiz sistem fail ext2/ext3/ext4

## Overview
Perintah `resize2fs` digunakan untuk mengubah saiz sistem fail yang menggunakan format ext2, ext3, atau ext4. Ia membolehkan pengguna untuk mengembangkan atau mengurangkan saiz sistem fail tanpa kehilangan data.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `resize2fs`:

```
resize2fs [options] [arguments]
```

## Common Options
- `-f` : Memaksa pengubahsuaian saiz walaupun sistem fail tidak bersedia.
- `-p` : Menunjukkan kemajuan semasa proses pengubahsuaian saiz.
- `-s` : Mengubah saiz sistem fail tanpa mengubah saiz partition.
- `-M` : Mengurangkan saiz sistem fail ke saiz minimum yang mungkin.

## Common Examples
Berikut adalah beberapa contoh penggunaan `resize2fs`:

1. **Mengembangkan saiz sistem fail ke saiz partition maksimum:**
   ```bash
   resize2fs /dev/sda1
   ```

2. **Mengubah saiz sistem fail kepada 20G:**
   ```bash
   resize2fs /dev/sda1 20G
   ```

3. **Mengurangkan saiz sistem fail dengan memaksa:**
   ```bash
   resize2fs -f /dev/sda1 10G
   ```

4. **Menunjukkan kemajuan semasa proses pengubahsuaian:**
   ```bash
   resize2fs -p /dev/sda1
   ```

## Tips
- Sebelum menggunakan `resize2fs`, pastikan untuk membuat salinan sandaran data penting.
- Pastikan sistem fail tidak sedang digunakan semasa proses pengubahsuaian untuk mengelakkan kerosakan data.
- Gunakan `resize2fs -M` untuk mengurangkan saiz sistem fail ke minimum yang mungkin, tetapi pastikan tiada data yang akan hilang.