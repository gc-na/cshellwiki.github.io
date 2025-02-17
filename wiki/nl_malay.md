# [Linux] Bash nl Penggunaan: Menambah Nombor Baris pada Fail Teks

## Overview
Perintah `nl` dalam Bash digunakan untuk menambah nombor baris pada fail teks. Ia membolehkan pengguna untuk melihat dan menguruskan kandungan fail dengan lebih mudah, terutamanya apabila berurusan dengan fail yang panjang.

## Usage
Berikut adalah sintaks asas untuk menggunakan perintah `nl`:

```bash
nl [options] [arguments]
```

## Common Options
- `-b` : Menentukan cara nombor baris ditambah (contohnya, `-b a` untuk menambah nombor pada setiap baris).
- `-f` : Menentukan baris yang akan dimulakan dengan nombor (contohnya, `-f 2` untuk mula dari baris kedua).
- `-n` : Menentukan format nombor (contohnya, `-n ln` untuk nombor kiri).
- `-w` : Menentukan lebar nombor (contohnya, `-w 5` untuk lebar 5 karakter).

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `nl`:

1. Menambah nombor baris pada fail teks:
   ```bash
   nl fail.txt
   ```

2. Menambah nombor pada setiap baris dan menyimpan output ke fail baru:
   ```bash
   nl -b a fail.txt > fail_nombor.txt
   ```

3. Menggunakan pilihan untuk mula menambah nombor dari baris kedua:
   ```bash
   nl -f 2 fail.txt
   ```

4. Menentukan format nombor dan lebar:
   ```bash
   nl -n ln -w 5 fail.txt
   ```

## Tips
- Gunakan pilihan `-b` untuk mengawal baris mana yang akan dinomborkan, terutamanya berguna untuk fail yang mempunyai tajuk.
- Simpan output ke dalam fail baru jika anda ingin mengekalkan fail asal tanpa perubahan.
- Eksperimen dengan pilihan `-n` dan `-w` untuk mendapatkan format nombor yang sesuai dengan keperluan anda.