# [Linux] Bash tune2fs Penggunaan: Mengubah parameter sistem fail ext2/ext3/ext4

## Overview
Perintah `tune2fs` digunakan untuk mengubah parameter sistem fail pada sistem fail ext2, ext3, dan ext4. Ia membolehkan pengguna untuk menyesuaikan pelbagai aspek sistem fail, seperti pengaturan pemulihan, pengurusan ruang, dan lain-lain.

## Usage
Berikut adalah sintaks asas untuk perintah `tune2fs`:

```bash
tune2fs [options] [arguments]
```

## Common Options
- `-c <count>`: Menetapkan bilangan maksimum pengubahsuaian yang dibenarkan sebelum sistem fail perlu diperiksa.
- `-i <interval>`: Menetapkan selang masa antara pemeriksaan sistem fail.
- `-m <percentage>`: Menetapkan peratusan ruang yang boleh digunakan untuk pengguna root.
- `-O <feature>`: Mengaktifkan ciri tertentu pada sistem fail.
- `-L <label>`: Menetapkan label untuk sistem fail.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan `tune2fs`:

1. **Menetapkan bilangan maksimum pengubahsuaian:**
   ```bash
   tune2fs -c 20 /dev/sda1
   ```

2. **Menetapkan selang masa pemeriksaan kepada 30 hari:**
   ```bash
   tune2fs -i 30d /dev/sda1
   ```

3. **Mengaktifkan ciri 'dir_index':**
   ```bash
   tune2fs -O dir_index /dev/sda1
   ```

4. **Menetapkan label untuk sistem fail:**
   ```bash
   tune2fs -L MyLabel /dev/sda1
   ```

## Tips
- Selalu buat salinan sandaran data penting sebelum mengubah parameter sistem fail.
- Gunakan perintah `tune2fs -l /dev/sda1` untuk melihat maklumat dan parameter semasa sistem fail.
- Pastikan sistem fail tidak sedang digunakan semasa melakukan perubahan untuk mengelakkan kerosakan data.