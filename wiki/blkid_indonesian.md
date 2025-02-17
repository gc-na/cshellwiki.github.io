# [Linux] Bash blkid Penggunaan: Menampilkan informasi sistem file

## Overview
Perintah `blkid` digunakan untuk menampilkan informasi tentang perangkat blok, seperti partisi dan sistem file yang ada di sistem. Ini sangat berguna untuk mengetahui UUID, tipe sistem file, dan label dari perangkat penyimpanan.

## Usage
Sintaks dasar dari perintah `blkid` adalah sebagai berikut:

```
blkid [options] [arguments]
```

## Common Options
- `-o` : Menentukan format output (misalnya, `value`, `full`, `list`).
- `-s` : Menentukan atribut yang ingin ditampilkan (misalnya, `UUID`, `TYPE`).
- `-p` : Mengabaikan cache dan membaca informasi langsung dari perangkat.
- `-c` : Menentukan file cache yang akan digunakan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `blkid`:

1. Menampilkan semua informasi perangkat blok:
   ```bash
   blkid
   ```

2. Menampilkan informasi dalam format nilai:
   ```bash
   blkid -o value
   ```

3. Menampilkan hanya UUID dari semua perangkat:
   ```bash
   blkid -s UUID
   ```

4. Menampilkan informasi spesifik untuk perangkat tertentu:
   ```bash
   blkid /dev/sda1
   ```

5. Mengabaikan cache dan mendapatkan informasi terbaru:
   ```bash
   blkid -p
   ```

## Tips
- Gunakan opsi `-o value` untuk mendapatkan output yang lebih bersih dan mudah dibaca.
- Jika Anda sering menggunakan `blkid`, pertimbangkan untuk membuat alias di shell Anda untuk mempercepat akses.
- Pastikan untuk menjalankan `blkid` dengan hak akses yang sesuai jika Anda tidak melihat semua perangkat.