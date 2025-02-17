# [Linux] Bash history Penggunaan: Menunjukkan senarai arahan yang telah digunakan

## Overview
Perintah `history` dalam Bash digunakan untuk memaparkan senarai arahan yang telah dijalankan dalam sesi terminal. Ini membolehkan pengguna untuk melihat semula arahan yang telah digunakan dan mengulangi arahan tersebut dengan mudah.

## Usage
Berikut adalah sintaks asas untuk perintah `history`:

```bash
history [options] [arguments]
```

## Common Options
- `-c`: Menghapuskan semua sejarah arahan.
- `-d offset`: Menghapuskan arahan pada kedudukan tertentu dalam sejarah.
- `n`: Menunjukkan hanya `n` arahan terakhir.

## Common Examples
Berikut adalah beberapa contoh penggunaan perintah `history`:

1. **Melihat semua arahan dalam sejarah:**
   ```bash
   history
   ```

2. **Melihat 10 arahan terakhir:**
   ```bash
   history 10
   ```

3. **Mengulangi arahan tertentu menggunakan nombor sejarah:**
   ```bash
   !100
   ```
   (Ini akan menjalankan arahan yang berada pada kedudukan 100 dalam sejarah.)

4. **Menghapuskan arahan tertentu dari sejarah:**
   ```bash
   history -d 100
   ```
   (Ini akan menghapuskan arahan pada kedudukan 100.)

5. **Menghapuskan semua sejarah arahan:**
   ```bash
   history -c
   ```

## Tips
- Gunakan `Ctrl + R` untuk mencari arahan dalam sejarah dengan cepat.
- Sentiasa semak sejarah sebelum menjalankan arahan yang sama untuk mengelakkan kesilapan.
- Simpan sejarah arahan yang penting dengan menggunakan `history > filename.txt` untuk menyimpan ke dalam fail.