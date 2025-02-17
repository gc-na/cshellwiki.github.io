# [Linux] Bash script Penggunaan: Merekam sesi terminal

## Overview
Perintah `script` digunakan untuk merekam sesi terminal ke dalam sebuah file. Ini sangat berguna untuk mencatat perintah yang dijalankan dan output yang dihasilkan selama sesi terminal, sehingga Anda dapat mereview atau membagikannya nanti.

## Usage
Berikut adalah sintaks dasar dari perintah `script`:

```bash
script [options] [file]
```

## Common Options
- `-a`: Menambahkan output ke file yang sudah ada, bukan menimpa file.
- `-c`: Menjalankan perintah yang ditentukan dan merekam outputnya.
- `-f`: Menampilkan output ke layar secara real-time saat merekam.
- `-q`: Menjalankan dalam mode diam, tanpa menampilkan pesan pembuka atau penutup.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `script`:

1. **Merekam sesi terminal ke file default:**

   ```bash
   script
   ```

   Ini akan mulai merekam sesi terminal dan menyimpannya ke file bernama `typescript`.

2. **Merekam sesi dengan nama file tertentu:**

   ```bash
   script mysession.txt
   ```

   Ini akan merekam sesi ke dalam file `mysession.txt`.

3. **Menambahkan output ke file yang sudah ada:**

   ```bash
   script -a mysession.txt
   ```

   Ini akan menambahkan output ke file `mysession.txt` yang sudah ada.

4. **Merekam output dari perintah tertentu:**

   ```bash
   script -c "ls -l" output.txt
   ```

   Ini akan menjalankan perintah `ls -l` dan merekam outputnya ke dalam file `output.txt`.

5. **Merekam sesi dengan tampilan real-time:**

   ```bash
   script -f mysession.txt
   ```

   Ini akan merekam sesi dan menampilkan output ke layar secara real-time.

## Tips
- Selalu periksa file hasil rekaman setelah sesi selesai untuk memastikan semua informasi yang diperlukan telah tercatat.
- Gunakan opsi `-q` jika Anda tidak ingin melihat pesan pembuka atau penutup saat merekam.
- Pertimbangkan untuk menggunakan opsi `-a` jika Anda ingin merekam beberapa sesi ke dalam file yang sama tanpa kehilangan data sebelumnya.