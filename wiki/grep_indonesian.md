# [Linux] Bash grep Penggunaan: Mencari pola dalam teks

## Overview
Perintah `grep` adalah alat yang sangat berguna dalam Bash untuk mencari pola tertentu dalam file atau output dari perintah lain. Dengan menggunakan ekspresi reguler, `grep` dapat membantu Anda menemukan baris yang sesuai dengan kriteria yang ditentukan.

## Usage
Sintaks dasar dari perintah `grep` adalah sebagai berikut:
```
grep [options] [arguments]
```

## Common Options
Berikut adalah beberapa opsi umum yang sering digunakan dengan `grep`:

- `-i`: Mengabaikan perbedaan antara huruf besar dan kecil.
- `-v`: Menampilkan baris yang tidak cocok dengan pola.
- `-r`: Mencari secara rekursif dalam direktori.
- `-n`: Menampilkan nomor baris dari hasil pencarian.
- `-l`: Menampilkan nama file yang mengandung pola yang dicari.

## Common Examples
Berikut adalah beberapa contoh penggunaan `grep`:

1. Mencari kata "error" dalam file `log.txt`:
   ```bash
   grep "error" log.txt
   ```

2. Mencari kata "warning" tanpa memperhatikan huruf besar/kecil:
   ```bash
   grep -i "warning" log.txt
   ```

3. Menampilkan baris yang tidak mengandung kata "success":
   ```bash
   grep -v "success" log.txt
   ```

4. Mencari secara rekursif untuk kata "config" dalam semua file di direktori saat ini:
   ```bash
   grep -r "config" .
   ```

5. Menampilkan nomor baris saat mencari kata "TODO" dalam file `script.sh`:
   ```bash
   grep -n "TODO" script.sh
   ```

## Tips
- Gunakan opsi `-i` untuk memudahkan pencarian tanpa memperhatikan huruf besar/kecil.
- Kombinasikan `grep` dengan perintah lain menggunakan pipe (`|`) untuk menyaring output, misalnya `dmesg | grep "usb"`.
- Simpan hasil pencarian ke dalam file dengan menggunakan redirection, contohnya: `grep "error" log.txt > hasil.txt`.