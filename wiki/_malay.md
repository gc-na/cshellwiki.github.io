# [Linux] Bash @ penggunaan: [menjalankan perintah dalam latar belakang]

## Overview
Perintah `@` dalam Bash digunakan untuk menjalankan perintah dalam latar belakang, membolehkan pengguna untuk terus menggunakan terminal tanpa menunggu perintah tersebut selesai.

## Usage
Sintaks asas untuk perintah ini adalah seperti berikut:

```
@ [options] [arguments]
```

## Common Options
- `&` : Menjalankan perintah dalam latar belakang.
- `jobs` : Menunjukkan senarai perintah yang sedang berjalan di latar belakang.
- `fg` : Mengembalikan perintah yang berjalan di latar belakang ke latar depan.
- `bg` : Menjalankan perintah yang dihentikan di latar depan ke latar belakang.

## Common Examples
Berikut adalah beberapa contoh praktikal menggunakan perintah ini:

1. Menjalankan skrip dalam latar belakang:
   ```bash
   ./myscript.sh &
   ```

2. Menjalankan perintah `sleep` selama 10 saat dalam latar belakang:
   ```bash
   sleep 10 &
   ```

3. Menunjukkan semua perintah yang sedang berjalan di latar belakang:
   ```bash
   jobs
   ```

4. Mengembalikan perintah yang dihentikan ke latar depan:
   ```bash
   fg %1
   ```

5. Menjalankan perintah yang dihentikan di latar depan ke latar belakang:
   ```bash
   bg %1
   ```

## Tips
- Sentiasa gunakan `&` di akhir perintah untuk memastikan ia berjalan di latar belakang.
- Gunakan `jobs` untuk memantau perintah yang sedang berjalan di latar belakang.
- Jika anda ingin menghentikan perintah yang berjalan di latar belakang, gunakan `kill` diikuti dengan ID proses.