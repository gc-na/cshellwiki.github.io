# [Sistem Operasi] C Shell (csh) who <Penggunaan>: Menampilkan pengguna yang sedang masuk

## Overview
Perintah `who` digunakan untuk menampilkan daftar pengguna yang saat ini sedang masuk ke sistem. Informasi yang ditampilkan termasuk nama pengguna, terminal yang digunakan, waktu masuk, dan alamat IP (jika tersedia).

## Usage
Berikut adalah sintaks dasar dari perintah `who`:

```
who [options] [arguments]
```

## Common Options
- `-a`: Menampilkan semua informasi yang tersedia, termasuk pengguna yang tidak aktif.
- `-b`: Menampilkan waktu terakhir sistem di-reboot.
- `-q`: Menampilkan hanya nama pengguna yang sedang aktif dan jumlah total pengguna.
- `-r`: Menampilkan informasi tentang runlevel saat ini.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `who`:

1. Menampilkan semua pengguna yang sedang masuk:
   ```csh
   who
   ```

2. Menampilkan semua informasi termasuk pengguna yang tidak aktif:
   ```csh
   who -a
   ```

3. Menampilkan waktu terakhir sistem di-reboot:
   ```csh
   who -b
   ```

4. Menampilkan hanya nama pengguna yang sedang aktif dan jumlah total pengguna:
   ```csh
   who -q
   ```

5. Menampilkan informasi tentang runlevel saat ini:
   ```csh
   who -r
   ```

## Tips
- Gunakan opsi `-q` untuk mendapatkan ringkasan cepat tentang pengguna yang sedang aktif.
- Kombinasikan `who` dengan perintah lain seperti `grep` untuk mencari pengguna tertentu.
- Perintah `who` dapat membantu dalam pemecahan masalah jika Anda perlu mengetahui siapa yang sedang menggunakan sistem saat ini.