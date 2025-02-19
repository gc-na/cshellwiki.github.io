# [Sistem Operasi] C Shell (csh) stty: Mengatur terminal dan pengaturan input/output

## Overview
Perintah `stty` digunakan untuk mengubah dan mengatur pengaturan terminal di sistem Unix dan Linux. Ini memungkinkan pengguna untuk mengkonfigurasi bagaimana terminal berinteraksi dengan input dan output, termasuk pengaturan karakter khusus dan pengaturan mode.

## Usage
Berikut adalah sintaks dasar dari perintah `stty`:

```
stty [options] [arguments]
```

## Common Options
- `-a` : Menampilkan semua pengaturan terminal saat ini.
- `-g` : Menampilkan pengaturan terminal dalam format yang dapat digunakan kembali.
- `erase` : Mengatur karakter yang digunakan untuk menghapus karakter sebelumnya.
- `kill` : Mengatur karakter yang digunakan untuk menghapus seluruh baris.
- `intr` : Mengatur karakter yang digunakan untuk menghentikan proses yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `stty`:

1. **Menampilkan pengaturan terminal saat ini:**
   ```csh
   stty -a
   ```

2. **Mengatur karakter penghapus menjadi Ctrl+H:**
   ```csh
   stty erase ^H
   ```

3. **Mengatur karakter kill menjadi Ctrl+U:**
   ```csh
   stty kill ^U
   ```

4. **Mengatur karakter interupsi menjadi Ctrl+C:**
   ```csh
   stty intr ^C
   ```

5. **Menyimpan pengaturan terminal saat ini ke dalam variabel:**
   ```csh
   set terminal_settings = `stty -g`
   ```

## Tips
- Selalu periksa pengaturan terminal saat ini dengan `stty -a` sebelum melakukan perubahan.
- Gunakan `stty -g` untuk menyimpan pengaturan terminal yang dapat digunakan kembali, sehingga Anda dapat mengembalikannya jika diperlukan.
- Hati-hati saat mengubah pengaturan terminal, karena beberapa perubahan dapat mempengaruhi cara Anda berinteraksi dengan shell.