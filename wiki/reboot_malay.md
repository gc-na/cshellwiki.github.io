# [Linux] Bash reboot Penggunaan: Memulakan semula sistem

## Overview
Perintah `reboot` digunakan untuk memulakan semula sistem operasi Linux. Ia menghentikan semua proses yang sedang berjalan dan memulakan semula komputer, menjadikannya berguna untuk mengaplikasikan perubahan konfigurasi atau selepas pemasangan kemas kini.

## Usage
Sintaks asas bagi perintah `reboot` adalah seperti berikut:
```
reboot [options] [arguments]
```

## Common Options
Berikut adalah beberapa pilihan biasa untuk perintah `reboot`:

- `-f` : Memulakan semula sistem tanpa menghentikan proses dengan betul.
- `-p` : Mematikan kuasa selepas memulakan semula.
- `-w` : Menulis maklumat reboot ke dalam fail log tetapi tidak memulakan semula sistem.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `reboot`:

1. **Memulakan semula sistem secara normal:**
   ```bash
   reboot
   ```

2. **Memulakan semula sistem tanpa menghentikan proses dengan betul:**
   ```bash
   reboot -f
   ```

3. **Menulis maklumat reboot ke dalam log tanpa memulakan semula:**
   ```bash
   reboot -w
   ```

4. **Memulakan semula sistem dan mematikan kuasa selepas itu:**
   ```bash
   reboot -p
   ```

## Tips
- Pastikan anda menyimpan semua kerja sebelum menggunakan perintah `reboot` untuk mengelakkan kehilangan data.
- Gunakan pilihan `-f` dengan berhati-hati, kerana ia boleh menyebabkan kehilangan data jika proses tidak dihentikan dengan betul.
- Untuk memulakan semula sistem pada waktu tertentu, anda boleh menggunakan perintah `shutdown` dengan pilihan `-r` dan waktu yang ditetapkan.