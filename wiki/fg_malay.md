# [Linux] Bash fg Penggunaan: Mengembalikan proses ke latar depan

## Overview
Perintah `fg` dalam Bash digunakan untuk mengembalikan proses yang sedang berjalan di latar belakang ke latar depan. Ini berguna apabila anda ingin berinteraksi dengan proses tersebut setelah memindahkannya ke latar belakang.

## Usage
Sintaks asas untuk perintah `fg` adalah seperti berikut:

```
fg [options] [arguments]
```

## Common Options
- `job_id`: Menentukan ID pekerjaan yang ingin dibawa ke latar depan. Jika tidak ditentukan, `fg` akan membawa pekerjaan terakhir yang dihentikan ke latar depan.
- `-l`: Menunjukkan senarai semua pekerjaan yang sedang berjalan.

## Common Examples
Berikut adalah beberapa contoh penggunaan `fg`:

1. **Mengembalikan pekerjaan terakhir ke latar depan:**
   ```bash
   fg
   ```

2. **Mengembalikan pekerjaan tertentu ke latar depan menggunakan job ID:**
   ```bash
   fg %1
   ```

3. **Menunjukkan senarai pekerjaan yang sedang berjalan:**
   ```bash
   jobs
   ```

4. **Mengembalikan pekerjaan kedua dalam senarai ke latar depan:**
   ```bash
   fg %2
   ```

## Tips
- Sentiasa semak senarai pekerjaan yang sedang berjalan dengan perintah `jobs` sebelum menggunakan `fg` untuk memastikan anda membawa proses yang betul ke latar depan.
- Jika anda sering menggunakan `fg`, pertimbangkan untuk menggunakan `bg` untuk menjalankan proses di latar belakang tanpa menghentikannya terlebih dahulu.