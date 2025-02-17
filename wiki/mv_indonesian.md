# [Linux] Bash mv Penggunaan: Memindahkan atau Mengganti Nama Berkas

## Overview
Perintah `mv` dalam Bash digunakan untuk memindahkan berkas atau direktori dari satu lokasi ke lokasi lain. Selain itu, perintah ini juga dapat digunakan untuk mengganti nama berkas atau direktori.

## Usage
Berikut adalah sintaks dasar dari perintah `mv`:

```bash
mv [options] [arguments]
```

## Common Options
- `-i`: Menanyakan konfirmasi sebelum menimpa berkas yang ada.
- `-u`: Hanya memindahkan berkas jika berkas sumber lebih baru daripada berkas tujuan atau jika berkas tujuan tidak ada.
- `-v`: Menampilkan informasi tentang berkas yang sedang dipindahkan.
- `-n`: Tidak menimpa berkas yang sudah ada.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `mv`:

1. **Memindahkan berkas ke direktori lain:**
   ```bash
   mv file.txt /path/to/directory/
   ```

2. **Mengganti nama berkas:**
   ```bash
   mv oldname.txt newname.txt
   ```

3. **Memindahkan beberapa berkas sekaligus:**
   ```bash
   mv file1.txt file2.txt /path/to/directory/
   ```

4. **Memindahkan berkas dengan konfirmasi:**
   ```bash
   mv -i file.txt /path/to/directory/
   ```

5. **Menampilkan proses pemindahan:**
   ```bash
   mv -v file.txt /path/to/directory/
   ```

## Tips
- Selalu gunakan opsi `-i` jika Anda khawatir tentang menimpa berkas yang ada.
- Periksa kembali jalur direktori tujuan untuk memastikan berkas dipindahkan ke lokasi yang benar.
- Gunakan opsi `-u` untuk menghindari pemindahan berkas yang tidak perlu, terutama saat bekerja dengan banyak berkas.