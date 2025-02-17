# [Linux] Bash cmp Penggunaan: Membandingkan file biner

## Overview
Perintah `cmp` digunakan untuk membandingkan dua file biner byte demi byte. Jika ada perbedaan antara file yang dibandingkan, `cmp` akan menunjukkan lokasi perbedaan tersebut. Ini sangat berguna untuk memeriksa integritas file atau memastikan bahwa dua file identik.

## Usage
Berikut adalah sintaks dasar dari perintah `cmp`:

```bash
cmp [options] [file1] [file2]
```

## Common Options
- `-l`: Menampilkan byte yang berbeda dalam format numerik.
- `-s`: Tidak menampilkan output, hanya mengembalikan status keluar.
- `-i OFFSET`: Mengabaikan byte awal dari file pertama.
- `-n N`: Hanya membandingkan N byte pertama dari file.

## Common Examples
Berikut adalah beberapa contoh penggunaan `cmp`:

1. **Membandingkan dua file**:
   ```bash
   cmp file1.bin file2.bin
   ```

2. **Membandingkan dua file dan menampilkan byte yang berbeda**:
   ```bash
   cmp -l file1.bin file2.bin
   ```

3. **Membandingkan dua file tanpa output, hanya status keluar**:
   ```bash
   cmp -s file1.bin file2.bin
   ```

4. **Membandingkan hanya 10 byte pertama dari dua file**:
   ```bash
   cmp -n 10 file1.bin file2.bin
   ```

## Tips
- Gunakan opsi `-s` jika Anda hanya ingin mengetahui apakah file berbeda tanpa melihat detailnya.
- Jika Anda bekerja dengan file besar, pertimbangkan untuk menggunakan opsi `-n` untuk membatasi jumlah byte yang dibandingkan.
- `cmp` sangat berguna dalam skrip untuk memeriksa apakah file telah berhasil disalin atau diunduh tanpa kesalahan.